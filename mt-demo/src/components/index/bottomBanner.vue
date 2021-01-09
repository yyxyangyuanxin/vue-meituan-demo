<template>
  <ul>
    <li>
      <a href="#">
        <img src="http://p1.meituan.net/codeman/8cce56c467a17e04f3094d1e455462a0132772.png" alt />
      </a>
    </li>
    <li>
      <a href="#">
        <img src="http://p1.meituan.net/codeman/16442c19da1f1c4544f794e29d99c92051716.jpg" alt />
      </a>
    </li>
    <li>
      <a href="#">
        <img src="http://p1.meituan.net/codeman/5b21cddb4bb1cbc3a9c3bce0f726c75940469.jpg" alt />
      </a>
    </li>
  </ul>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
ul {
  display: flex;
  li:nth-child(1),
  li:nth-child(2) {
    a {
      img {
        width: 270px;
        height: 165px;
        background-size: 270px;
        background-position: 50%;
        background-repeat: no-repeat;
        margin-top: 10px;
        margin-right: 10px;
      }
    }
  }
  li:nth-child(3) {
    a {
      img {
        width: 150px;
        height: 165px;
        margin-top: 10px;
        margin-right: 10px;
        background-size: 150px;
        background-position: 50%;
        background-repeat: no-repeat;
        background-color: #fff;
      }
    }
  }
}
</style>