<template>
  <div>
    <swiper loop auto :show-desc-mask=false :show-dots=false :list="list" :index="list" :aspect-ratio="1000/800" ref="swiper" class="test"></swiper>
    <div class="enter-box">
      <p class="enter-title" @click="showMore">这里是预约入口<i :class="[iconfont,iconType]"></i></p>
    </div>
  </div>
</template>

<script>
import { Swiper } from 'vux'
export default {
  name: 'Home',
  data () {
    return {
      iconfont: 'iconfont',
      iconType: 'icon-shangyige',
      list: [
        {
          url: 'javascript:',
          img: 'static/img/home/identification_c.jpg',
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: 'static/img/home/personal_c.jpg',
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: 'static/img/home/pressional_c.jpg',
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: 'static/img/home/marry_c.jpg',
          title: '证件照'
        }
      ]
    }
  },
  methods: {
    showMore () {
      this.iconType = this.iconType === 'icon-shangyige' ? 'icon-moreunfold' : 'icon-shangyige'
      let anchor = this.$el.querySelector('test')
      console.log(anchor)
      console.log(this.$refs.swiper.xheight)
      console.log(this.$refs.swiper.$el.offsetTop)
      console.log(document.documentElement.clientHeight)
    }
  },
  components: {
    Swiper
  }
}
</script>

<style scoped>
.enter-box {
  z-index: 99;
  position: absolute;
  bottom: 0px;
  width: 100%;
  height: calc(100vh - 1033.5px);
  background: #ccc;
}
.enter-title {
  padding-left: 15px;
  line-height: calc(100vh - 1033.5px);
  letter-spacing: 5px;
  font-weight: bolder;
}
</style>
