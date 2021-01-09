<template>
  <div class="index-box">
    <div class="banner-box">
      <div class="menu">
        <my-menu />
      </div>
      <div class="banner">
        <banner />
      </div>
      <div class="banner-card">
        <banner-card />
      </div>
    </div>
    <div class="container">
      <container />
    </div>
  </div>
</template>

<script>
import myMenu from "@/components/index/menu.vue";
import banner from "@/components/index/banner.vue";
import bannerCard from "@/components/index/bannerCard.vue";
import container from "@/components/index/container.vue";

export default {
  components: {
    myMenu,
    banner,
    bannerCard,
    container
  }
};
</script>

<style lang='less' scoped>
.index-box {
  width: 1190px;
  margin: 0 auto;
  .banner-box {
    display: flex;
    justify-content: space-between;
    .menu {
      width: 228px;
    }
    .banner {
      width: 710px;
    }
    .banner-card {
      margin-top: 10px;
    }
  }
}
</style>