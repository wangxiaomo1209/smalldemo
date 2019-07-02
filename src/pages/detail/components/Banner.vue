<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/1904/a2/a23ae48aac0c0ab2a3.water.jpg_600x330_405288ba.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">西溪国家湿地洪园</div>
      </div>
    </div>
    <common-gallary
      :imgs="imgs"
      v-show="showGallary"
      @close="handleGallaryClose"
    ></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: ['//img1.qunarzz.com/sight/p0/1907/fe/fe656739f7f059c1a3.water.jpg_600x330_7867789e.jpg', '//img1.qunarzz.com/sight/p0/1907/fe/fe656739f7f059c1a3.water.jpg_600x330_7867789e.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    overflow: hidden
    height: 0
    padding-bottom: 55%
    position relative
    .banner-img
      width:100%
    .banner-info
      display: block
      position:absolute
      left: 0
      right: 0
      bottom: 0
      color:#fff
      padding: 0 0 .2rem .2rem
      background-image: linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0,0.8))
      .banner-title
        flex: 1
        font-size: .36rem
</style>
