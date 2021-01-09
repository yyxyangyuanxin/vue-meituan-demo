<template>
  <div class="banner-card-box">
    <div class="banner-card-top">
      <div class="card-img-top">
        <img src="//s0.meituan.net/bs/fe-web-meituan/e350c4a/img/avatar.jpg" alt />
      </div>
      <p class="user-name">Hi！你好</p>
      <el-button round>注册</el-button>
      <el-button round>立刻登录</el-button>
    </div>
    <div class="banner-card-bottom">
      <div class="card-img-bottom">
        <img src="//s1.meituan.net/bs/fe-web-meituan/60ac9a0/img/download-qr.png" alt />
      </div>
      <p class="app-name">美团APP手机版</p>
      <p class="sl">
        <span class="red">1元起</span>
        <span class="gary">吃喝玩乐</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.banner-card-box {
  .banner-card-top {
    box-sizing: border-box;
    padding-top: 30px;
    width: 228px;
    height: 238px;
    background-color: #fff;
    border: 1px solid #e5e5e5;
    display: flex;
    flex-direction: column;
    align-items: center;
    .card-img-top {
      border-radius: 30px;
      margin: 0px auto 4px auto;
      img {
        width: 47px;
        height: 47px;
        border-radius: 50%;
        border: 4px solid #e5e5e5;
      }
    }
    p {
      font-size: 16px;
      color: #222;
      text-align: center;
      font-weight: 500;
      white-space: nowrap;
      width: 6em;
      overflow: hidden;
      text-overflow: ellipsis;
      margin: 0 auto;
    }
    .el-button{
        width: 120px;
        height: 40px;
        margin: 5px auto 7.5px auto;
    }
  }
  .banner-card-bottom {
    width: 228px;
    height: 165px;
    margin-top: 10px;
    background-color: #fff;
    border: 1px solid #e5e5e5;
    text-align: center;
    .card-img-bottom {
        margin-top: 10px;
      img {
        width: 95px;
        height: 95px;
      }
    }
    .app-name {
      font-size: 16px;
      color: #222222;
      font-weight: 500;
    }
    .sl {
      font-size: 12px;
      font-weight: 500;
      margin-top: 2px;
      .red {
        color: #ec5330;
        margin-right: 5px;
      }
      .gary {
        color: #3f3f3f;
      }
    }
  }
}
</style>