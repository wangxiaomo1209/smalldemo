<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :list="list"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '推荐',
        children: [{
          title: '西溪湿地成人门车船联票',
          children: [{
            title: '西溪湿地成人门车船联票(龙蛇嘴主入口)'
          }]
        }, {
          title: '西溪湿地成人门车船票'
        }, {
          title: '西溪湿地成人门票'
        }]
      }, {
        title: '门票'
      }, {
        title: '一日游'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem
</style>
