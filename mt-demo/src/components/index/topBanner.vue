<template>
  <div class="banner-box">
    <my-carousel />
    <a href="#">
      <img src="http://p0.meituan.net/codeman/e473bb428f070321269b23370ff02ba956209.jpg" alt />
    </a>
  </div>
</template>

<script>
import myCarousel from "./carousel.vue";
export default {
  components: {
    myCarousel,
  }
};
</script>

<style lang='less' scoped>
.banner-box {
  position: relative;
  a {
    width: 150px;
    position: absolute;
    left: 550px;
    img {
      width: 150px;
      height: 240px;
      margin-left: 10px;
      margin-right: 10px;
      background-size: 150px;
      background-position: 50%;
      background-repeat: no-repeat;
      background-color: #fff;
    }
  }
}
</style>