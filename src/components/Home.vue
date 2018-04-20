<template>
  <div>
    <swiper loop auto :show-desc-mask=false :show-dots=false :list="list" :index="list" :aspect-ratio="1000/800" ref="swiper" class="test"></swiper>
    <div :class="enterBoxClass">
      <div class="enter-container">
        <p :class="[ isAction ? enterTitleAction : enterTitle ]" @click="showMore">这里是预约入口<i :class="[iconfont, isAction ? iconDown : iconLeft ]"></i></p>
        <div class="line"></div>
        <collapse-transition>
            <div class="select-box" v-show="isAction"></div>
        </collapse-transition>
      </div>
    </div>
  </div>
</template>

<script>
import { Swiper } from 'vux'
import CollapseTransition from '@/components/CollapseTransition'

export default {
  name: 'Home',
  data () {
    return {
      enterBoxClass: 'enter-box',
      enterTitle: 'enter-title',
      enterTitleAction: 'enter-title-action',
      iconfont: 'iconfont',
      iconLeft: 'icon-shangyige',
      iconDown: 'icon-moreunfold',
      isAction: false,
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
      this.enterBoxClass = this.enterBoxClass === 'enter-box' ? 'enter-box-action' : 'enter-box'
      let anchor = this.$el.querySelector('test')
      this.isAction = !this.isAction
      console.log(anchor)
      console.log(this.$refs.swiper.xheight)
      console.log(this.$refs.swiper.$el.offsetTop)
      console.log(document.documentElement.clientHeight)
    }
  },
  components: {
    Swiper,
    CollapseTransition
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
  color: #232323;
  background: #ccc;
  transition-duration: 1s;
  transition-property: all;
}
.enter-box-action {
  z-index: 99;
  position: absolute;
  bottom: 0px;
  width: 100%;
  height: calc(100vh - 903.5px);
  background: #ccc;
  transition-duration: 1s;
  transition-property: all;
}
.enter-container {
  margin: 0px auto;
  width: 90%;
}
.enter-title {
  line-height: calc(100vh - 1033.5px);
  letter-spacing: 5px;
  font-weight: bolder;
  transition-duration: 0.5s;
  transition-property: line-height;
}
.enter-title-action {
  line-height: 120px;
  letter-spacing: 5px;
  font-weight: bolder;
  transition-duration: 0.5s;
  transition-property: line-height;
}
.line {
  margin-bottom: 15px;
  width: 100%;
  height: 5px;
  background-color: #232323;
}
.select-box {
  width: 100%;
  height: 130px;
  background-color: #fff;
}
</style>
