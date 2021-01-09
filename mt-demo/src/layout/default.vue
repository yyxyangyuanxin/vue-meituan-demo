<template>
  <div class="default-box">
    <header>
      <top-bar />
      <search-bar />
    </header>
    <div class="main">
      <router-view />
    </div>
    <footer>
      <my-footer />
    </footer>
  </div>
</template>

<script>
import topBar from "@/components/header/topBar.vue";
import searchBar from "@/components/header/searchBar.vue";
import myFooter from "@/components/footer/index.vue";
export default {
  components: {
    topBar,
    searchBar,
    myFooter
  }
};
</script>

<style lang='less' scoped>
.default-box {
  .main {
    background: #f8f8f8;
  }
}
</style>