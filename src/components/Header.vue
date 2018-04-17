<template>
  <div>
    <flexbox justify="space-between" align="center">
      <flexbox-item >
        <i class="iconfont icon-shangyige"></i>
      </flexbox-item>
      <flexbox-item :span="8">
        <img src="../assets/img/logo_white.png" alt="logo" class="header-logo">
      </flexbox-item>
      <flexbox-item >
        <i class="iconfont icon-yonghu"></i>
      </flexbox-item>
    </flexbox>
  </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
div {
  height: 96px;
  text-align: center;
  background-color: #ed6825;
}
.header-logo {
  padding-top: 3%;
  height: 60px;
}
.iconfont {
  font-size: 60px;
  color: #fff;
}
</style>

