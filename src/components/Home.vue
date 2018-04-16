<template>
  <div>
    <swiper loop auto show-dots=false show-desc-mask=false dots-position="center" :list="list" :index="list" :aspect-ratio="1000/800"></swiper>
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
          img: require('../assets/img/home/identification_c.jpg'),
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: require('../assets/img/home/personal_c.jpg'),
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: require('../assets/img/home/pressional_c.jpg'),
          title: '证件照'
        },
        {
          url: 'javascript:',
          img: require('../assets/img/home/marry_c.jpg'),
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
