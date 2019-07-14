<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f3/d51669250308cc.jpg_r_640x214_7a127cd0.jpg',
        title: '宝华山国家森林公园',
        desc: '这里最近很火哦，好多人十多年房价的设计费你说的！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1811/58/a02ad3ab47e3e3.jpg_r_640x214_08977098.jpg',
        title: '千华古村',
        desc: '镇江本月收藏Top5╰(￣▽￣)╭'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/f1/ae9d4299b8aaea.jpg_r_640x214_0c555905.jpg',
        title: '金山',
        desc: '金山有“神话山”之称，名胜古迹众多'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .4rem
    line-height: 2.16rem
    background: #eee
    text-indent: 1rem
  .item-img-wrapper
    height: 0
    overflow: hidden
    padding-bottom: 33.9%
    .item-img
      width: 100%
  .item-info
    padding: 1rem
    .item-title
      line-height: 2.6rem
      font-size: 1.2rem
    .item-desc
      line-height: 1rem
      color: #ccc
</style>
