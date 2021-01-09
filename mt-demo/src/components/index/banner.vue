<template>
  <div class="banner-box">
    <div class="top-banner">
      <top-banner />
    </div>
    <div class="bottom-banner">
      <bottom-banner />
    </div>
  </div>
</template>

<script>
import topBanner from "./topBanner.vue";
import bottomBanner from "./bottomBanner.vue";
export default {
  components: {
    topBanner,
    bottomBanner
  }
};
</script>

<style lang='less' scoped>
.banner-box {
   display: flex;
    flex-direction: column;
  .top-banner {
    height: 240px;
    margin-top: 10px;
  }
}
</style>