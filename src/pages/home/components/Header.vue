<template>
  <div class="header">
  <div class="header-left">
    <div class="iconfont back-icon">&#xe624;</div>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题
  </div>
  <router-link to="/city">
    <div class="header-right">
      {{this.$store.state.city}}
      <span class="iconfont arrow-icon">&#xe64a;</span>
    </div>
  </router-link>
  </div>
</template>

<script>
export default{
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  line-height:0.86rem
  display:flex
  background:$bgColor
  color:#fff
  .header-left
    width :0.64rem
    float left
    .back-icon
      text-align:center
      font-size:.4rem
  .header-input
    flex:1
    line-height .64rem
    height:.64rem
    margin-top:.12rem
    height:.64rem
    margin-left:.2rem
    padding-left .2rem
    background :#fff
    border-radius:.1rem
    color:#ccc
  .header-right
    width:1.24rem
    float:right
    text-align:center
    color: white
    .arrow-icon
      margin-left :-.04rem
      font-size:.24rem
</style>
