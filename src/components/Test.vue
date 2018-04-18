<template>
  <div>
      <div :class="className">
          <p>点击我</p>
      </div>
      <button @click="change">ccc</button>
      <button @click="changeh">hei</button>
  </div>
</template>

<script>
export default {
  name: 'Test',
  data () {
    return {
      className: 'container'
    }
  },
  methods: {
    change () {
      this.className = 'container-action'
    },
    changeh () {
      this.className = 'container'
    }
  }
}
</script>

<style scoped>
.container {
  width: 100%;
  height: 90px;
  transition: width 2s;
  -moz-transition: width 2s; /* Firefox 4 */
  -webkit-transition: width 2s; /* Safari 和 Chrome */
  -o-transition: width 2s; /* Opera */
  background-color: #ccc;
}
.container-action {
  width: 100px;
  transition: width 2s;
  -moz-transition: width 2s; /* Firefox 4 */
  -webkit-transition: width 2s; /* Safari 和 Chrome */
  -o-transition: width 2s; /* Opera */
  background-color: #ccc;
  height: 90px;
}
</style>
