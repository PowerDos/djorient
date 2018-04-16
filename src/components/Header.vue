<template>
  <div>
    {{msg}}
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      msg: '头部'
    }
  }
}
</script>

<style scoped>
div{
  font-size: 20px;
}
</style>

