<template>
  <div class="menu-list">
    <dl class="nav-text">
      <dt>
        <h2 class="nav-title">全部分类</h2>
      </dt>
      <dd
        class="nav-item"
        v-for="(nav,index) in menuList"
        :key="nav.id"
        @mouseenter="addMouseenter(index)"
        @mouseleave="addMouseleave(index)"
      >
        <a href="#" target="_blank">{{ nav.navName }}</a>
        <span class="iconfont2">&#xe612;</span>
        <dl class="nav-detail-box" v-if="nav.children.isShowDetail">
          <dt>
            <div>
              <h2 class="detail-title">
                <a href="#">{{ nav.navName }}</a>
              </h2>
              <a href="#" class="iconfont2 more">更多&#xe612;</a>
            </div>
          </dt>
          <dd class="detail-item" v-for="(item, index) in nav.children.detailText" :key="index">
            <a href="#">{{ item }}</a>
          </dd>
        </dl>
      </dd>
    </dl>
  </div>
</template>

<script>
export default {
  data() {
    return {
      menuList: [
        {
          id: 1,
          navName: "美食",
          children: {
            isShowDetail: false,
            detailText: [
              "代金券",
              "甜点饮品",
              "火锅",
              "自助餐",
              "小吃快餐",
              "日韩料理",
              "西餐",
              "聚餐宴请",
              "烧烤烤肉",
              "东北菜",
              "川湘菜",
              "江浙菜",
              "香锅烤鱼",
              "粤港菜",
              "中式烧烤/烤串",
              "西北菜",
              "咖啡酒吧",
              "茶馆云贵菜",
              "东南亚菜",
              "海鲜素食",
              "台湾/客家菜",
              "创意菜",
              "汤/粥/炖菜",
              "蒙餐新疆菜",
              "其他美食",
              "京菜鲁菜"
            ]
          }
        },
        {
          id: 2,
          navName: "外卖",
          children: {
            isShowDetail: false,
            detailText: [
              "美团外卖"
            ]
          }
        },
        {
          id: 3,
          navName: "酒店HOT",
          children: {
            isShowDetail: false,
            detailText: [
              "经济型",
              "舒适/三星",
              "高档/四星",
              "豪华/五星"
            ]
          }
        },
        {
          id: 4,
          navName: "民宿",
          children: {
            isShowDetail: false,
            detailText:[
              "上海",
              "成都",
              "北京",
              "重庆",
              "南京",
              "杭州",
              "广州",
              "西安",
              "武汉",
              "厦门",
              "长沙",
              "青岛",
              "深圳",
              "天津",
              "苏州"
            ]
          }
        },
        {
          id: 5,
          navName: "猫眼电影",
          children: {
            isShowDetail: false,
            detailText: [
              "金逸影城",
              "万达影城",
              "大地影院",
              "哈艺时尚影城",
              "金逸影城",
              "万达影城",
              "大地影院",
              "哈艺时尚影城",
              "金逸影城",
              "万达影城",
              "大地影院",
              "哈艺时尚影城",
              "金逸影城",
              "万达影城",
              "大地影院",
              "哈艺时尚影城",
            ]
          }
        },
        {
          id: 6,
          navName: "机票 / 火车票",
          children: {
            isShowDetail: false,
            detailText:[
              "国内机票",
              "国际/港澳台机票"
            ]
          }
        },
        {
          id: 7,
          navName: "休闲娱乐 / KTV",
          children: {
            isShowDetail: false,
            detailText:[
              "足疗",
              "按摩",
              "洗浴/汗蒸",
              "酒吧",
              "密室",
              "逃脱",
              "足疗",
              "按摩",
              "洗浴/汗蒸",
              "酒吧",
              "密室",
              "逃脱",
              "足疗",
              "按摩",
              "洗浴/汗蒸",
              "酒吧",
              "密室",
              "逃脱",
              "足疗",
              "按摩",
              "洗浴/汗蒸",
              "酒吧",
              "密室",
              "逃脱",
            ]
          }
        },
        {
          id: 8,
          navName: "生活服务",
          children: {
            isShowDetail: false,
            detailText:[
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
              "衣物/皮具",
              "洗护",
              "家政",
              "搬家",
              "运输",
              "送水",
            ]
          }
        },
        {
          id: 9,
          navName: "丽人 / 美发 / 医学美容",
          children: {
            isShowDetail: false,
            detailText: [
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 10,
          navName: "结婚 / 婚纱摄影 / 婚宴",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 11,
          navName: "亲子 / 儿童乐园 / 幼教",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 12,
          navName: "运动健身 / 健身中心",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 13,
          navName: "家装 / 建材 / 家居",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 14,
          navName: "学习培训 / 音乐培训",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 15,
          navName: "医疗健康 / 宠物 / 爱车",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        },
        {
          id: 16,
          navName: "酒吧 / 密室逃脱",
          children: {
            isShowDetail: false,
            detailText:[
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
              "美发",
              "美甲",
              "美睫",
              "美容",
              "美体",
              "医学",
              "美容",
              "瑜伽",
              "舞蹈",
            ]
          }
        }
      ]
    };
  },
  methods: {
    addMouseenter(index) {
      this.menuList[index].children.isShowDetail = true;
    },
    addMouseleave(index) {
      this.menuList[index].children.isShowDetail = false;
    }
  }
};
</script>

<style lang='less' scoped>
.menu-list {
  height: 475px;
  text-align: left;
  box-sizing: border-box;
  margin-top: -50px;
  z-index: 1000;
  color: #646464;
  background: #fff;
  box-sizing: border-box;
  border: 1px solid #e5e5e5;
  .nav-text {
    position: absolute;
    height: 425px;
    box-sizing: border-box;
    display: block;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    dt {
      .nav-title {
        height: 50px;
        padding-top: 15px;
        box-sizing: border-box;
        color: #222222;
        font-size: 16px;
        font-weight: 700;
        margin-left: 15px;
      }
    }
    .nav-item {
      position: relative;
      box-sizing: border-box;
      padding: 2px 12px;
      height: 26px;
      width: 228px;
      a {
        font-size: 13px;
        line-height: 20px;
        height: 20px;
        color: #646464;
        text-decoration: none;
      }
      span {
        float: right;
      }
      .nav-detail-box {
        position: absolute;
        top: 10px;
        left: 228px;
        width: 340px;
        padding: 0 30px;
        height: 416px;
        background-color: #fff;
        z-index: 199;
        color: #666;
        overflow: hidden;
        dt {
          div {
            margin-top: 24px;
            height: 22px;
            line-height: 22px;
            width: 340px;
            padding-bottom: 10px;
            border-bottom: 1px solid #e5e5e5;
            .detail-title {
              a {
                font-size: 16px;
                font-weight: 500;
                color: #222;
                float: left;
              }
            }
            .more {
              font-size: 12px;
              color: #999;
              font-weight: 400;
              float: right;
              position: relative;
            }
          }
        }
        .detail-item {
          display: inline-block;
          a {
            color: #999;
            font-size: 12px;
            line-height: 15px;
            display: inline-block;
            margin-right: 16px;
            margin-top: 10px;
            &:hover {
              color: #fe8c00;
            }
          }
        }
      }
    }
  }
}
</style>