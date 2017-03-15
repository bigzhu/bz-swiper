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
          spaceBetween: 100,
          autoplay: 3000,
          loop: true,
          pagination: '.swiper-pagination'
        }
        setTimeout(function () {
          let a = Swiper('.swiper-container', conf)
          console.log(a)
        }, 3)
      }
    }
  }
</script>
<style>
  .img.slide {
    width: 100%;
  }
  .white-bz {
    background-color: white;
  }
  .swiper-pagination {
    top: 85%;
    .swiper-pagination-bullet{ opacity: 1; }
    .swiper-pagination-bullet-active { background: white; opacity: 1; }
  }
</style>
