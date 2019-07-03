<template>
  <div>
    <div class="header-fixed">
      <router-link to="/">
        <div class="iconfont header-fixed-back">&#xe624;</div>
      </router-link>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header-fixed
    z-index: 2
    position: fixed
    top: 0
    left: 0
    right: 0
    height:.86rem
    line-height: .86rem
    text-align: center
    color: #fff
    background: $bgColor
    font-size: .32rem
    opacity: .8
    .header-fixed-back
      position: absolute
      top: 0
      left: 0
      width: .64rem
      text-align: center
      font-size: .4rem
      color: #fff
</style>
