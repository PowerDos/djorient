<template>
  <div>
    <swiper loop auto :show-desc-mask=false :show-dots=false :list="list" :index="list" :aspect-ratio="1000/800"></swiper>
  </div>
</template>

<script>
import { Swiper } from 'vux'
export default {
  name: 'Home',
  data () {
    return {
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
  components: {
    Swiper
  }
}
</script>

<style scoped>
.vux-indicator.custom-bottom {
  bottom: 30px;
}
</style>
