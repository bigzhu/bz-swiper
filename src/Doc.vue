<template>
  <div>
    <doc :name="name"
      :desc="desc"
      :parm_desc="parm_desc"
      :parms="parms"
      :code="code"
      >
      <bz :datas="datas"></bz>
    </doc>
  </div>
</template>
<script>
  import Bz from './Bz'
  import Doc from 'bz-doc'
  export default {
    components: {
      Bz,
      Doc
    },
    data: function () {
      return {
        name: 'bz-swiper',
        desc: '登录页面',
        datas: [
          {url: '/bigzhu', src: 'https://m.gotosiam.com/static/img/home-slide-01.8e9068a.jpg'},
          {url: '/bigzhu', src: 'https://m.gotosiam.com/static/img/home-slide-02.f47b925.jpg'}
        ],
        parms: [
          {parm: 'datas', desc: '一个list, ojbect 有 url 和 src 两个字段'}
        ],
        parm_desc: ``,
        code: `<bz :datas="datas"></bz>`
      }
    },
    methods: {
    }
  }
</script>
