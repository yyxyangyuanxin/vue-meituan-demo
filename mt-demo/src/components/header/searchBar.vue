<template>
  <div class="box">
    <div class="search-bar-box">
      <div class="logo">
        <img src="@/assets/images/logo.png" alt />
      </div>
      <div class="search-module">
        <div class="input-block">
          <input
            type="text"
            placeholder="搜索商家或地点"
            v-model="searchText"
            @focus="bundleFocus"
            @blur="bundleBlur"
          />
          <button class="search-button">
            <i class="iconfont">&#xe6d1;</i>
          </button>
          <div class="search-suggest" v-if="isSearchList">
            <h6 v-if="isSuggestList">热门搜索</h6>
            <dl v-else>
              <dd v-for="suggestList in suggestListArr" :key="suggestList.id">
                <a href="#">{{ suggestList.name }}</a>
              </dd>
            </dl>
          </div>
        </div>
      </div>
      <div class="nav">
        <ul>
          <li>
            <router-link to="/" tag="a">美团外卖</router-link>
          </li>
          <li>
            <router-link to="/" tag="a">猫眼电影</router-link>
          </li>
          <li>
            <router-link to="/" tag="a">美团酒店</router-link>
          </li>
          <li>
            <router-link to="/" tag="a">民宅&nbsp;/&nbsp;公寓</router-link>
          </li>
          <li>
            <router-link to="/" tag="a">商家入驻</router-link>
          </li>
          <li>
            <router-link to="/" tag="a">美团公益</router-link>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      searchText: "",
      isSearchList: false,
      suggestListArr: [
        {
          name: "火锅 海底捞",
          id: 1,
        },
        {
          name: "火锅自助餐",
          id: 2,
        },
        {
          name: "火锅 牛杂",
          id: 3,
        },
        {
          name: "火龙果",
          id: 4,
        },
      ],
    };
  },
  computed: {
    isSuggestList() {
      return !this.searchText;
    },
  },
  methods: {
    bundleFocus() {
      this.isSearchList = true;
    },
    bundleBlur() {
      this.isSearchList = false;
    },
  },
};
</script>

<style lang='less' scoped>
.box {
  background: #fff;
  .search-bar-box {
    width: 1190px;
    height: 122px;
    margin: 0 auto;
    display: flex;
    padding-bottom: 35px;
    z-index: 1;
    .logo {
      float: left;
      padding-top: 28px;
      padding-right: 60px;
      padding-bottom: 40px;
      font-size: 16px;
      min-width: 220px;
      height: 54px;
      box-sizing: content-box;
      vertical-align: sub;
      img {
        width: 126px;
        height: 46px;
      }
    }
    .search-module {
      float: left;
      padding-top: 28px;
      position: absolute;
      left: 50%;
      transform: translate(-50%);
      z-index: 999;
      .input-block {
        width: 550px;
        height: 40px;
        input {
          border: 1px solid #e5e5e5;
          outline: none;
          border-right: none;
          border-radius: 4px 0 0 4px;
          line-height: 100%;
          box-sizing: border-box;
          display: inline-block !important;
          padding: 15px;
          font-size: 14px;
          width: 85.45%;
          height: 100%;
        }
        .search-button {
          outline: none;
          width: 14.55%;
          box-sizing: border-box;
          line-height: 100%;
          height: 100%;
          background: #ffc300;
          border: none;
          float: right;
          color: #222222;
          cursor: pointer;
          border-bottom-right-radius: 4px;
          border-top-right-radius: 4px;
          i {
            line-height: 100%;
          }
        }
        .search-suggest {
          width: 85.45%;
          // display: none;
          box-sizing: border-box;
          position: absolute;
          border: 1px solid #e5e5e5;
          border-top: none;
          background: #fff;
          z-index: 999;
          box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
          border-bottom-left-radius: 4px;
          border-bottom-right-radius: 4px;
          color: #999;
          font-size: 12px;
          text-align: left;
          h6 {
            margin: 0;
            padding: 10px;
            padding-bottom: 5px;
            font-size: 1em;
            color: #999;
            height: 51px;
          }
          dl {
            dd {
              a {
                padding: 3px 10px;
                color: #333;
                line-height: 25px;
              }
            }
          }
        }
      }
    }
    .nav {
      margin-top: 120px;
      height: 35px;
      ul {
        li {
          float: left;
          a {
            color: #222;
            font-weight: 700;
            font-size: 16px;
            margin: 0 20px;
            text-decoration: none;
            cursor: pointer;
            position: relative;
            &:hover {
              color: #ed1e24;
            }
          }
        }
      }
    }
  }
}
</style>