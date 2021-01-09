<template>
  <div class="rec-box">
    <div class="title-container">
      <div class="title">推荐民宿</div>
      <ul class="nav">
        <li
          :class="{active:curIndex === index}"
          @mouseenter="curIndex = index"
          v-for="(nav,index) in navList"
          :key="nav.id"
        >{{ nav.navName }}</li>
      </ul>
    </div>
    <div class="minsu-view-box clearfix">
      <div class="minsu-list" v-if="0 === curIndex">
        <minsu-view v-for="minsu in minsuList" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="1 === curIndex">
        <minsu-view v-for="minsu in minsuList2" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="2 === curIndex">
        <minsu-view v-for="minsu in minsuList3" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="3 === curIndex">
        <minsu-view v-for="minsu in minsuList" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="4 === curIndex">
        <minsu-view v-for="minsu in minsuList2" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="5 === curIndex">
        <minsu-view v-for="minsu in minsuList3" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="6 === curIndex">
        <minsu-view v-for="minsu in minsuList" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="7 === curIndex">
        <minsu-view v-for="minsu in minsuList2" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="8 === curIndex">
        <minsu-view v-for="minsu in minsuList3" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="9 === curIndex">
        <minsu-view v-for="minsu in minsuList" :key="minsu.id" v-bind="minsu" />
      </div>
      <div class="minsu-list" v-else-if="10 === curIndex">
        <minsu-view v-for="minsu in minsuList3" :key="minsu.id" v-bind="minsu" />
      </div>
    </div>
  </div>
</template>

<script>
import minsuView from "./minsuView";
export default {
  data() {
    return {
      curIndex: 0,
      navList: [
        {
          navName: "深圳",
          id: 1
        },
        {
          navName: "珠海",
          id: 2
        },
        {
          navName: "桂林",
          id: 3
        },
        {
          navName: "北海",
          id: 4
        },
        {
          navName: "海口",
          id: 5
        },
        {
          navName: "惠州",
          id: 6
        },
        {
          navName: "佛山",
          id: 7
        },
        {
          navName: "东莞",
          id: 8
        },
        {
          navName: "柳州",
          id: 9
        },
        {
          navName: "清远",
          id: 10
        }
      ],
      minsuList: [
        {
          id: 1,
          src:
            "https://img.meituan.net/phoenix/6f028847c9f5c1d0b6d669e1fdfdff3943338.jpg@740w_416h_1e_1c",
          productTitle: "深圳北站龙兴公寓大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 108
        },
        {
          id: 2,
          src:
            "https://img.meituan.net/phoenix/2eea8dc888da1ee28cdde6d26efd47cd3240362.jpg@740w_416h_1e_1c",
          productTitle:
            "宝安国际机场/固戍地铁站/后瑞地铁站/温馨公寓/简约家居风/西湾滨海公园/西湾红树林/华胜实验学校公交站/三围社区",
          subTitle: "整套1居室·可住2人 |民治",
          price: 158
        },
        {
          id: 3,
          src:
            "https://img.meituan.net/phoenix/e1d66d936eee1b8ddf59caf5c713d1f72334898.jpg@740w_416h_1e_1c",
          productTitle: "【鹏城悦里·名城汇】现代风格复式公寓 /舒适榻榻米床",
          subTitle: "整套1居室·可住2人 |民治",
          price: 368
        },
        {
          id: 4,
          src:
            "http://p0.meituan.net/iphoenix/e82f346e66185a2a46cefb120d2d0b041567852.jpg@740w_416h_1e_1c",
          productTitle:
            "”4号线红山地铁口“Loft复式两房，旁边就是“九方商城”，4号线一站直达深圳北站，直达福田口岸",
          subTitle: "整套1居室·可住2人 |民治",
          price: 400
        },
        {
          id: 5,
          src:
            "https://img.meituan.net/iphoenix/484ddd4f06d7a2c29ad3aaffce1ef11012221216.jpg@740w_416h_1e_1c",
          productTitle:
            "【现代loft一居室】深圳北站HBC汇隆中心/近地铁可直达会展中心、福田中心、香港+电梯+管家服务",
          subTitle: "整套1居室·可住2人 |民治",
          price: 315
        },
        {
          id: 6,
          src:
            "http://p1.meituan.net/iphoenix/afe8141941966fb3f6477592cf11746c132232.jpg@740w_416h_1e_1c",
          productTitle: "栖居国际公寓/特价大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 106
        }
      ],
      minsuList2: [
        {
          id: 1,
          src:
            "https://img.meituan.net/phoenix/dd5c49a8f0274874dbb186334c4abc64372904.jpg@740w_416h_1e_1c",
          productTitle: "深圳北站龙兴公寓大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 108
        },
        {
          id: 2,
          src:
            "https://img.meituan.net/phoenix/8c36770a556a874bbc1b18efc1a23c3c1748853.jpg@740w_416h_1e_1c",
          productTitle:
            "宝安国际机场/固戍地铁站/后瑞地铁站/温馨公寓/简约家居风/西湾滨海公园/西湾红树林/华胜实验学校公交站/三围社区",
          subTitle: "整套1居室·可住2人 |民治",
          price: 158
        },
        {
          id: 3,
          src:
            "https://img.meituan.net/phoenix/d9505d8574bf74600dd035eff536967977057.jpg@740w_416h_1e_1c",
          productTitle: "【鹏城悦里·名城汇】现代风格复式公寓 /舒适榻榻米床",
          subTitle: "整套1居室·可住2人 |民治",
          price: 368
        },
        {
          id: 4,
          src:
            "https://img.meituan.net/iphoenix/67d5879a6c6a52fab8d4ffeffdc510e2596295.jpg@740w_416h_1e_1c",
          productTitle:
            "”4号线红山地铁口“Loft复式两房，旁边就是“九方商城”，4号线一站直达深圳北站，直达福田口岸",
          subTitle: "整套1居室·可住2人 |民治",
          price: 400
        },
        {
          id: 5,
          src:
            "https://img.meituan.net/phoenix/689d6e4a6a40cd51027c3d712a6c6f0e618395.jpg@740w_416h_1e_1c",
          productTitle:
            "【现代loft一居室】深圳北站HBC汇隆中心/近地铁可直达会展中心、福田中心、香港+电梯+管家服务",
          subTitle: "整套1居室·可住2人 |民治",
          price: 315
        },
        {
          id: 6,
          src:
            "https://img.meituan.net/phoenix/2625f45ed16ccb89e5e1e2b5c38499d0755412.jpg@740w_416h_1e_1c",
          productTitle: "栖居国际公寓/特价大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 106
        }
      ],
      minsuList3: [
        {
          id: 1,
          src:
            "http://p1.meituan.net/iphoenix/ca4389587e619cf31dc496acb0bacbf0305639.jpg@740w_416h_1e_1c",
          productTitle: "深圳北站龙兴公寓大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 108
        },
        {
          id: 2,
          src:
            "https://img.meituan.net/phoenix/954fdf88a74ca302930807c5f0a9d0e0123185.jpg@740w_416h_1e_1c",
          productTitle:
            "宝安国际机场/固戍地铁站/后瑞地铁站/温馨公寓/简约家居风/西湾滨海公园/西湾红树林/华胜实验学校公交站/三围社区",
          subTitle: "整套1居室·可住2人 |民治",
          price: 158
        },
        {
          id: 3,
          src:
            "https://img.meituan.net/phoenix/6d6d71031c7570b669c6bc2112956dbf1639811.jpg@740w_416h_1e_1c",
          productTitle: "【鹏城悦里·名城汇】现代风格复式公寓 /舒适榻榻米床",
          subTitle: "整套1居室·可住2人 |民治",
          price: 368
        },
        {
          id: 4,
          src:
            "https://img.meituan.net/phoenix/f1269cf7393ce19ffd5288140039fb2d413343.jpg@740w_416h_1e_1c",
          productTitle:
            "”4号线红山地铁口“Loft复式两房，旁边就是“九方商城”，4号线一站直达深圳北站，直达福田口岸",
          subTitle: "整套1居室·可住2人 |民治",
          price: 400
        },
        {
          id: 5,
          src:
            "https://img.meituan.net/phoenix/c9ab7e364e97ed74326f26ee3a101b80442854.jpg@740w_416h_1e_1c",
          productTitle:
            "【现代loft一居室】深圳北站HBC汇隆中心/近地铁可直达会展中心、福田中心、香港+电梯+管家服务",
          subTitle: "整套1居室·可住2人 |民治",
          price: 315
        },
        {
          id: 6,
          src:
            "http://p0.meituan.net/iphoenix/96f97d594ef0d806c37f57e300a08fe2436057.jpg@740w_416h_1e_1c",
          productTitle: "栖居国际公寓/特价大床房",
          subTitle: "整套1居室·可住2人 |民治",
          price: 106
        }
      ]
    };
  },
  components: {
    minsuView
  }
};
</script>

<style lang='less' scoped>
.rec-box {
  .title-container {
    background: linear-gradient(
        to right,
        rgb(243, 182, 74) 2%,
        rgb(242, 197, 69) 97%
      )
      rgb(243, 182, 74);
    width: 100%;
    height: 44px;
    line-height: 44px;
    box-sizing: border-box;
    font-size: 14px;
    color: #fff;
    border-top-right-radius: 5px;
    border-top-left-radius: 5px;
    margin-top: 40px;
    display: flex;
    .title {
      font-size: 18px;
      margin-left: 13px;
      margin-right: 10px;
    }
    .nav {
      li {
        float: left;
        padding: 0 5px;
        position: relative;
        cursor: pointer;
        text-transform: uppercase;
        &.active::after {
          position: absolute;
          border-left: 5px solid transparent;
          border-right: 5px solid transparent;
          border-bottom: 7px solid #fff;
          content: "";
          display: block;
          width: 2px;
          height: 0;
          top: 37px;
          left: 0;
          right: 0;
          margin: auto;
          opacity: 1;
        }
      }
    }
  }
  .minsu-view-box {
    padding: 20px;
    padding-right: 0;
    padding-bottom: 0;
    border: 1px solid #e5e5e5;
    border-top: 0px;
    border-bottom-left-radius: 4px;
    border-bottom-right-radius: 4px;
    background: #fff;
    .minsu-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      padding-right: 20px;
    }
  }
}
</style>