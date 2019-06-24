<template>
  <div>
    <div class="title">猜你喜欢</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1904/a2/a23ae48aac0c0ab2a3.water.jpg_200x200_38cef490.jpg',
        title: '西溪国家湿地洪园',
        desc: '308条评论',
        moneys: '70',
        place: '杭州'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1903/e0/e0e0c6ca274ad49aa3.img.jpg_200x200_0f072efb.jpg',
        title: '西溪国家湿地公园·周家村',
        desc: '17013条评论',
        moneys: '460',
        place: '西湖区'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1810/cc/cc47164357acbeb5a3.water.jpg_200x200_151f0405.jpg',
        title: '杭州云曼温泉',
        desc: '1332条评论',
        moneys: '4158',
        place: '萧山区'
      }]
    }
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
