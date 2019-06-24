<template>
  <div>
    <div class="title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <p class="item-money">
            ￥<strong class="moneys">{{item.moneys}}</strong>起
            <span class="item-place">{{item.place}}</span>
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  line-height: .8rem
  margin-top:.2rem
  background :#F5F5F5
  text-indent: .2rem
.item
  display :flex
  height: 1.9rem
  overflow: hidden
  .item-img
    width:1.7rem
    height:1.7rem
    padding:.1rem
  .item-info
    flex:1
    padding:.1rem
    min-width:0
    .item-title
      line-height:.54rem
      font-size:.32rem
      ellipsis()
    .item-desc
      line-height:.4rem
      color:#ccc
      ellipsis()
    .item-money
      color:#FF8300
      padding:.2rem 0
      .moneys
        font-size:.4rem
      .item-place
        float:right
        color:#000
</style>
