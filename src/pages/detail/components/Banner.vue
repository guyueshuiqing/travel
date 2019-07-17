<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/201403/07/7cee59b291070950a9cc5c9445b45eb5.jpg_600x330_b30214e3.jpg">
      <div class="banner-info">
        <div class="banner-title">宝华山国家森林公园(AAAA景区)</div>
        <div class="banner-number"><span class="iconfont banner-icon">&#xe6df;</span>4</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="hanldeGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      showGallary: false,
      imgs: ['http://img1.qunarzz.com/sight/p0/201403/07/f67ed52f569a9441a66a4f09064a6818.jpg_350x240_ee82645f.jpg', 'http://img1.qunarzz.com/sight/p0/201403/07/ffcf67147cb9a3063e5a69a8d64922ba.jpg_350x240_05bc476f.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    hanldeGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    color: #fff
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: 1.1rem
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, .8))
      .banner-title
        flex: 1
        padding: 0 .8rem
      .banner-number
        margin: .1rem auto
        padding: 0 1rem
        height: .9rem
        line-height: .9rem
        border-radius: .6rem
        background: rgba(0, 0, 0, .2)
        font-size: .6rem
        .banner-icon
          font-size: .6rem
          padding: 0 .2rem
</style>
