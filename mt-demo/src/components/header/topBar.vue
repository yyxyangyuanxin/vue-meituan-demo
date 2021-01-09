<template>
  <div class="top-bar-box">
    <div class="top-bar-container">
      <div class="geo">
        <geo />
      </div>
      <div class="my-nav">
        <my-nav />
      </div>
    </div>
  </div>
</template>

<script>
import geo from "./geo.vue";
import myNav from "./nav.vue";
export default {
  components: {
    geo,
    myNav
  }
};
</script>

<style lang='less' scoped>
.top-bar-box {
  align-items: center;
  width: 100%;
  background: #f8f8f8;
  font-size: 12px;
  color: #999;
  height: 40px;
  .top-bar-container{
    width: 1190px;
    margin: 0 auto;
    position: relative;
  }
  .geo{
    float: left;
    line-height: 40px;
  }
  .my-nav {
    float: right;
  }
}
</style>