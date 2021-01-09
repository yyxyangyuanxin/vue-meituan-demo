<template>
  <div>
    <a href="#">
      <img :src="src" />
      <div class="product-info">
        <p class="product-title">{{ productTitle }}</p>
        <p class="sub-title">
          <span>{{ subTitle }}</span>
        </p>
        <p class="price-number numfont price">
          <span class="price-icon">￥</span>
          {{ price }}
        </p>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    src: String,
    productTitle: String,
    subTitle: String,
    price: Number
  },
  data() {
    return {};
  }
};
</script>

<style lang='less' scoped>
div {
  img {
    width: 370px;
    height: 208px;
    border-radius: 4px;
    background: url(//p0.meituan.net/travelcube/214b841….png);
    background-size: cover;
    background-position: 50%;
    max-width: 100%;
    height: 208px;
    margin-bottom: 11px;
    cursor: pointer;
  }
  .product-info {
    text-align: left;
    padding-bottom: 25px;
    .product-title {
      font-size: 16px;
      color: #222222;
      overflow: hidden;
      white-space: nowrap;
      text-overflow: ellipsis;
      margin: 7px 0;
      font-weight: 400;
      width: 297px;
    }
    .sub-title {
      font-size: 12px;
      color: #999;
      text-align: left;
    }
    .price {
      font-weight: 500;
      font-size: 22px;
      color: #ff6600;
      letter-spacing: -0.8px;
      padding: 4px 0;
      .price-icon {
        font-size: 14px;
      }
    }
  }
}
</style>