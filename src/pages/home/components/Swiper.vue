<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: '//img10.360buyimg.com/img/jfs/t1/40605/39/6859/75627/5d075e90E747fb2ce/8f99540bd9c62218.jpg'
      }, {
        id: '0002',
        imgUrl: '//m.360buyimg.com/img/jfs/t1/34016/31/13800/99724/5d075e41E04e1180c/d8a5ee1de3f1043b.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background:white !important
.wrapper
  width:100%
  height:0
  overflow hidden
  padding-bottom:65%
  background:#eee
  .swiper-img
    width :100%
</style>
