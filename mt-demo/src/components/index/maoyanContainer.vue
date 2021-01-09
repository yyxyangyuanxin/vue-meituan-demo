<template>
  <div class="maoyan-box">
    <div class="btn pre" @click="bundlePre()">
        <i class="iconfont3">&#xe64e;</i>
    </div>
    <div class="btn next" @click="bundleNext()">
        <i class="iconfont3">&#xe632;</i>
    </div>
    <ul class="maoyan-title">
      <li>猫眼电影</li>
      <li>即将上映</li>
      <li class="iconfont">全部&#xe612;</li>
    </ul>
    <div class="slider">
      <ul class="slider-content" :style="style">
        <li v-for="film in filmArr" :key="film.id">
          <a href="#">
            <img
              :src="film.src"
            />
            <div class="info">
              <b>
                <span>{{ film.personNum }}</span>
                人想看
              </b>
              <p>{{ film.filmName }}</p>
            </div>
          </a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
    data(){
        return{
            filmArr:[
                {
                    src: "//p0.meituan.net/movie/6adbe9c365a3aaadfb65910bc279bf6a3385927.jpg@321w_445h_1e_1c",
                    id:1,
                    personNum:2574,
                    filmName:"沉香"
                },
                {
                    src: "//p0.meituan.net/movie/f1210412ff52740cfbc3cca8212834bd406835.jpg@321w_445h_1e_1c",
                    id:2,
                    personNum:1262,
                    filmName:"致命复活"
                },
                {
                    src: "//p0.meituan.net/movie/a19913517ec4dd7b1e8c56a199ceaa4280560.jpg@321w_445h_1e_1c",
                    id:3,
                    personNum:12914,
                    filmName:"天下无拐"
                },
                {
                    src: "//p1.meituan.net/movie/eb37c5b78ec0c14aaad707700fcc1443390529.jpg@321w_445h_1e_1c",
                    id:4,
                    personNum:2933,
                    filmName:"恋上美人鱼"
                },
                {
                    src: "//p1.meituan.net/movie/ccea56ae49249d482be5997aa98e94691344390.jpg@321w_445h_1e_1c",
                    id:5,
                    personNum:64929,
                    filmName:"拆弹专家2"
                },
                {
                    src: "//p1.meituan.net/movie/eb37c5b78ec0c14aaad707700fcc1443390529.jpg@321w_445h_1e_1c",
                    id:6,
                    personNum:2933,
                    filmName:"恋上美人鱼"
                },
                {
                    src: "//p1.meituan.net/movie/ccea56ae49249d482be5997aa98e94691344390.jpg@321w_445h_1e_1c",
                    id:7,
                    personNum:64929,
                    filmName:"拆弹专家2"
                },
                {
                    src: "//p0.meituan.net/movie/a19913517ec4dd7b1e8c56a199ceaa4280560.jpg@321w_445h_1e_1c",
                    id:8,
                    personNum:12914,
                    filmName:"天下无拐"
                },
                {
                    src: "//p0.meituan.net/movie/f1210412ff52740cfbc3cca8212834bd406835.jpg@321w_445h_1e_1c",
                    id:9,
                    personNum:1262,
                    filmName:"致命复活"
                },
                {
                    src: "//p0.meituan.net/movie/6adbe9c365a3aaadfb65910bc279bf6a3385927.jpg@321w_445h_1e_1c",
                    id:10,
                    personNum:2574,
                    filmName:"沉香"
                },
                {
                    src: "//p0.meituan.net/movie/6adbe9c365a3aaadfb65910bc279bf6a3385927.jpg@321w_445h_1e_1c",
                    id:11,
                    personNum:2574,
                    filmName:"沉香"
                },
                {
                    src: "//p0.meituan.net/movie/f1210412ff52740cfbc3cca8212834bd406835.jpg@321w_445h_1e_1c",
                    id:12,
                    personNum:1262,
                    filmName:"致命复活"
                },
                {
                    src: "//p0.meituan.net/movie/a19913517ec4dd7b1e8c56a199ceaa4280560.jpg@321w_445h_1e_1c",
                    id:13,
                    personNum:12914,
                    filmName:"天下无拐"
                },
                {
                    src: "//p1.meituan.net/movie/eb37c5b78ec0c14aaad707700fcc1443390529.jpg@321w_445h_1e_1c",
                    id:14,
                    personNum:2933,
                    filmName:"恋上美人鱼"
                },
                {
                    src: "//p1.meituan.net/movie/ccea56ae49249d482be5997aa98e94691344390.jpg@321w_445h_1e_1c",
                    id:15,
                    personNum:64929,
                    filmName:"拆弹专家2"
                },
            ],
            style:{
                left:0,
                width:'300%'
            }
        }
    },
    computed:{
       
    },
    methods:{
        bundlePre(){
            if(parseInt(this.style.left) === 0){
                return;
            }
            this.style.left = parseInt(this.style.left) + 100 + '%'
        },
        bundleNext(){
            if(parseInt(this.style.left) == (-parseInt(this.style.width) + 100)){
                return;
            }
            this.style.left = parseInt(this.style.left) - 100 + '%';
        }
    }
};
</script>

<style lang='less' scoped>
.maoyan-box {
  margin-top: 40px;
  position: relative;
  .btn {
      width: 40px;
      height: 40px;
      background: #333;
      position: absolute;
      z-index: 99;
      top: 50%;
      border-radius: 40px;
      opacity: 0;
      transition: opacity 0.5s;
      transform: scale(0.95);
      line-height: 40px;
      text-align: center;
      cursor: pointer;
    }
    &:hover .btn {
      opacity: 1;
    }
    .pre{
        i{
            margin-left: -2px;
        }
    }
    .next{
        right: 0;
        i{
            font-size: 28px;   
        }
    }
  .maoyan-title {
    background: linear-gradient(
        to right,
        rgb(250, 60, 104) 2%,
        rgb(254, 70, 77) 97%
      )
      rgb(250, 60, 104);
    width: 100%;
    height: 44px;
    line-height: 44px;
    box-sizing: border-box;
    font-size: 14px;
    color: #fff;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;
    li {
      &:nth-child(1) {
        font-size: 18px;
        margin-left: 13px;
        margin-right: 10px;
        float: left;
        padding: 0 5px;
        position: relative;
        cursor: pointer;
        text-transform: uppercase;
      }
      &:nth-child(2) {
        float: left;
        padding: 0 5px;
        position: relative;
        cursor: pointer;
        text-transform: uppercase;
        &::after {
          content: "";
          position: absolute;
          border-left: 5px solid transparent;
          border-right: 5px solid transparent;
          border-bottom: 7px solid #fff;
          display: block;
          width: 2px;
          height: 0;
          top: 37px;
          left: 0;
          right: 0;
          margin: auto;
        }
      }
      &:nth-child(3) {
        float: right;
        margin-right: 12px;
        padding: 0 5px;
        position: relative;
        cursor: pointer;
        text-transform: uppercase;
        font-size: 14px;
      }
    }
  }
  .slider {
    width: 100%;
    height: 100%;
    overflow: hidden;
    position: relative;
    margin: 0px 12px;
    .slider-content {
        position: relative;
        transition: left .5s;
      li {
        height: 297px;
        width: 214px;
        float: left;
        margin-right: 19px;
        background-size: 100%;
        background-repeat: no-repeat;
        background-position: 50%;
        position: relative;
        a {
          img {
            height: 100%;
            width: 100%;
            border-radius: 4px;
          }
          .info {
            height: 100px;
            width: 100%;
            position: absolute;
            bottom: 0;
            border-bottom-left-radius: 4px;
            border-bottom-right-radius: 4px;
            background-image: linear-gradient(
              -180deg,
              rgba(0, 0, 0, 0) 0%,
              rgba(29, 45, 55, 0.8) 99%
            );
            b {
              font-size: 12px;
              color: #fff;
              text-align: left;
              margin-top: 48px;
              padding-left: 10px;
              font-weight: 500;
              span {
                font-size: 16px;
                color: #fd9827;
                font-weight: 500;
              }
            }
            p {
              text-align: left;
              color: #fff;
              padding-left: 10px;
              font-size: 16px;
              white-space: nowrap;
              width: 6em;
              overflow: hidden;
              text-overflow: ellipsis;
              font-weight: 500;
            }
          }
        }
      }
    }
  }
}
</style>