<template>
  <div>
    <ul class="top-bar-nav">
      <li class="hover-select">
        <a href="#">我的美团</a>
        <dl class="my-mt-select common">
          <dd>
            <a href="#">我的订单</a>
          </dd>
          <dd>
            <a href="#">我的收藏</a>
          </dd>
          <dd>
            <a href="#">抵用券</a>
          </dd>
          <dd>
            <a href="#">账户设置</a>
          </dd>
        </dl>
      </li>
      <li>
        <a href="#">手机App</a>
      </li>
      <li class="hover-select">
        <a href="#">商家中心</a>
        <dl class="business-center common">
          <dd>
            <a href="#">美团餐饮商户中心</a>
          </dd>
          <dd>
            <a href="#">登录商家中心</a>
          </dd>
          <dd>
            <a href="#">美团智能收银</a>
          </dd>
          <dd>
            <a href="#">我想合作</a>
          </dd>
          <dd>
            <a href="#">手机免费开店</a>
          </dd>
          <dd>
            <a href="#">餐饮代理商招募</a>
          </dd>
          <dd>
            <a href="#">商家申请开票</a>
          </dd>
          <dd>
            <a href="#">免费合作美团排队</a>
          </dd>
        </dl>
      </li>
      <li class="hover-select">
        <a href="#">美团规则</a>
        <dl class="mt-rule common">
          <dd>
            <a href="#">规则中心</a>
          </dd>
          <dd>
            <a href="#">规则目录</a>
          </dd>
          <dd>
            <a href="#">规则评议院</a>
          </dd>
        </dl>
      </li>
      <li class="hover-select">
        <a href="#">网站导航</a>
        <div class="site-map-box common">
          <div class="site-map-list">
            <dl class="hotel-tourism">
              <dt>酒店旅游</dt>
              <dd>
                <a href="#">国际机票</a>
              </dd>
              <dd>
                <a href="#">火车票</a>
              </dd>
              <dd>
                <a href="#">名宿</a>
              </dd>
              <dd>
                <a href="#">经济型酒店</a>
              </dd>
              <dd>
                <a href="#">主题酒店</a>
              </dd>
              <dd>
                <a href="#">商务酒店</a>
              </dd>
              <dd>
                <a href="#">公寓</a>
              </dd>
              <dd>
                <a href="#">豪华酒店</a>
              </dd>
              <dd>
                <a href="#">客栈</a>
              </dd>
              <dd>
                <a href="#">青年旅社</a>
              </dd>
              <dd>
                <a href="#">度假酒店</a>
              </dd>
              <dd>
                <a href="#">别墅</a>
              </dd>
              <dd>
                <a href="#">农家院</a>
              </dd>
            </dl>
            <dl class="eat-cate">
              <dt>吃美食</dt>
              <dd>
                <a href="#">烤鱼</a>
              </dd>
              <dd>
                <a href="#">特色小吃</a>
              </dd>
              <dd>
                <a href="#">烧烤</a>
              </dd>
              <dd>
                <a href="#">自助餐</a>
              </dd>
              <dd>
                <a href="#">火锅</a>
              </dd>
              <dd>
                <a href="#">代金券</a>
              </dd>
            </dl>
            <dl class="see-movie">
              <dt>看电影</dt>
              <dd>
                <a href="#">热映电影</a>
              </dd>
              <dd>
                <a href="#">热门影院</a>
              </dd>
              <dd>
                <a href="#">热映电影口啤榜</a>
              </dd>
              <dd>
                <a href="#">最受期待电影</a>
              </dd>
              <dd>
                <a href="#">国内票房榜</a>
              </dd>
              <dd>
                <a href="#">北美票房榜</a>
              </dd>
              <dd>
                <a href="#">电影排行榜</a>
              </dd>
            </dl>
            <dl class="phone-app">
              <dt>手机应用</dt>
              <dd>
                <a href="#">
                  <img
                    class="appicon"
                    src="@/assets/images/appicons/meituan.png"
                    title="美团app"
                    alt="美团app"
                  />
                </a>
              </dd>
              <dd>
                <a href="#">
                  <img
                    class="appicon"
                    src="@/assets/images/appicons/waimai.png"
                    title="外卖app"
                    alt="外卖app"
                  />
                </a>
              </dd>
              <dd>
                <a href="#">
                  <img
                    class="appicon"
                    src="@/assets/images/appicons/162c3308d9622f6d9cfaa49e60be4dca8573.png"
                    title="民宿app"
                    alt="民宿app"
                  />
                </a>
              </dd>
              <dd>
                <a href="#">
                  <img
                    class="appicon"
                    src="@/assets/images/appicons/dianping.png"
                    title="民宿app"
                    alt="民宿app"
                  />
                </a>
              </dd>
              <dd>
                <a href="#">
                  <img
                    class="appicon"
                    src="@/assets/images/appicons/maoyan.png"
                    title="民宿app"
                    alt="民宿app"
                  />
                </a>
              </dd>
            </dl>
          </div>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.top-bar-nav {
  display: flex;
  a {
    color: #999;
    text-decoration: none;
  }
  a:hover {
    color: #fe8c00;
  }
  li {
    padding: 12px 14px;
    border-left: 1px solid transparent;
    border-right: 1px solid transparent;
    &.hover-select:hover {
      background-color: #fff;
      border-color: #e5e5e5;
      position: relative;
      height: 40px;
      box-sizing: border-box;
      box-shadow: 0 3px 5px 0 rgba(0, 0, 0, 0.1);
    }
    .my-mt-select,
    .business-center,
    .mt-rule {
      text-align: center;
      position: absolute;
    }
    .common {
      background: #fff;
      position: absolute;
      line-height: 35px;
      top: 39px;
      box-shadow: 0 4px 5px 0 rgba(0, 0, 0, 0.1);
      right: -1px;
      border: 1px solid #e5e5e5;
      border-top: 0;
      display: none;
      width: 100%;
      z-index: 1000;
    }
    &:nth-child(1):hover .my-mt-select {
      display: block;
    }
    &:nth-child(3):hover .business-center {
      display: block;
    }
    .business-center {
      width: 140%;
    }
    &:nth-child(4):hover .mt-rule {
      display: block;
    }
    &:nth-child(5):hover .site-map-box {
      display: block;
    }
    .site-map-box {
      width: 1200px;
      box-sizing: border-box;
      border-top-left-radius: 4px;
      padding: 30px 36px 36px 47px;
      .site-map-list {
        display: flex;
        position: relative;
        dt {
          margin-bottom: 26px;
          font-size: 14px;
          color: #222222;
          font-weight: 500;
          text-align: center;
        }
        .hotel-tourism,
        .eat-cate {
          margin-right: 47px;
        }
        .hotel-tourism {
          width: 234px;
          dd {
            float: left;
            width: 33%;
            text-align: center;
          }
        }
        .eat-cate {
          width: 156px;
          dd {
            width: 50%;
            text-align: center;
            float: left;
          }
        }
        .see-movie {
          width: 90px;
          text-align: center;
        }
        .phone-app {
          position: absolute;
          right: 47px;
          dd {
            float: left;
            margin: 0 8px;
            a {
              img {
                width: 60px;
                height: 60px;
              }
            }
          }
        }
      }
    }
  }
}
</style>