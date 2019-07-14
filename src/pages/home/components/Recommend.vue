<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1702/cd/cd0e6e561a6ff40fa3.water.jpg_200x200_1eb4fc81.jpg',
        title: '宝华山国家森林公园',
        desc: '这里最近很火哦，好多人十多年房价的设计费你说的！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1601/88/88f802d9fd4cbfad90.img.jpg_200x200_31aee11f.jpg',
        title: '千华古村',
        desc: '镇江本月收藏Top5╰(￣▽￣)╭'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1709/1d/1d9f37d9bfb300cfa3.water.jpg_200x200_edb8a4de.jpg',
        title: '金山',
        desc: '金山有“神话山”之称，名胜古迹众多'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/03/50b6fddd61f298eebbae4c0eb740ec71.jpg_200x200_8314fa46.jpg',
        title: '北固山',
        desc: '游人寻访三国遗迹的向往之地'
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
  .item
    overflow: hidden
    display: flex
    height: 8rem
    .item-img
      width: 7.2rem
      height: 7.2rem
      padding: .4rem
    .item-info
      position relative
      flex: 1
      padding: .4rem
      .item-title
        line-height: 2.6rem
        font-size: 1.2rem
      .item-desc
        line-height: 1rem
        color: #ccc
      .item-button
        position: absolute
        bottom: .8rem
        left: 1.2rem
        line-height: 1.5rem
        padding: 0 .8rem
        border-radius: .6rem
        color: #fff
        background-image: linear-gradient(130deg,#ffab1e 37%,#ff8c12 100%);
        text-align: center
</style>
