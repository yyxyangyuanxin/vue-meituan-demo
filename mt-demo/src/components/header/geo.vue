<template>
    <ul class="tap-bar-geo">
      <li>
        <i class="el-icon-location"></i>
      </li>
      <li>
        <span class="city">广州</span>
      </li>
      <li>
        <a href="#" class="chenge-city">切换城市</a>
      </li>
      <li>
        <div class="group-city">
          [
          <a href="#">佛山</a>
          <a href="#">顺德</a>
          <a href="#">南沙</a>]
        </div>
      </li>
      <li>
        <a href="#" class="login">立刻登录</a>
      </li>
      <li>
        <a href="#" class="register">注册</a>
      </li>
    </ul>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.tap-bar-geo {
  display: flex;
  .el-icon-location {
    color: #999;
  }
  .city {
    color: #666;
  }
  .chenge-city {
    background: #f4f4f4;
    border: 1px solid #e5e5e5;
    border-radius: 2px;
    color: #666;
    margin: 0 4px;
    padding: 0 2px;
    &:hover {
      color: #fe8c00;
      font-weight: 400;
    }
  }
  .group-city {
    a {
      margin: 0 4px;
      color: #999;
      &:hover{
          color: #FE8C00;
      }
    }
  }
  .login {
    color: #fe8c00;
    margin-left: 25px;
  }
  .register{
      color: #999;
      margin-left: 10px;
  }
}
</style>