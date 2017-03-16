<template>
  <div class="swiper-container">
    <div class="swiper-wrapper">
      <div v-for="d in datas" class="swiper-slide" >
        <a :href="d.url"><img class="img slide" :src="d.src"  alt=""></a>
      </div>
    </div>
    <div class="swiper-pagination"></div>
  </div>
</template>

<script>
  import 'swiper/dist/css/swiper.min.css'
  import Swiper from 'swiper'

  export default {
    props: {
      datas: {
        type: Array,
        default: []
      }
    },
    components: {
    },
    computed: {
    },
    data: function () {
      return {
      }
    },
    mounted: function () {
      this.$nextTick(function () {
        this.initSwiper()
      })
    },
    methods: {
      initSwiper: function () {
        let conf = {
          speed: 1400,
          autoplay: 3000,
          loop: true,
          pagination: '.swiper-pagination'
        }
        setTimeout(function () {
          Swiper('.swiper-container', conf)
        }, 3)
      }
    }
  }
</script>
