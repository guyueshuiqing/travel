<template>
  <div>
    <router-link tag="div" to="/" class="header-abs" v-show="showAbs">
      <div class="iconfont header-abs-back">&#xe624;</div>
    </router-link>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
      景点详情
      <router-link to="/">
        <div class="iconfont header-fixed-back">&#xe624;</div>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 50) {
        let opacity = top / 180
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header-abs
    position: absolute
    left: .5rem
    top: .5rem
    width: 2.2rem
    height: 2.2rem
    line-height: 2.2rem
    text-align: center
    border-radius: 1.1rem
    background: rgba(0, 0, 0, .8)
    .header-abs-back
      color: #fff
      font-size: 1.2rem
  .header-fixed
    position: fixed
    left: 0
    top: 0
    right: 0
    overflow: hidden
    height: $headerHeight
    line-height: $headerHeight
    font-size: 1.1rem
    text-align: center
    color: #fff
    background: $bgColor
    .header-fixed-back
      position: absolute
      left: 0
      top: 0
      text-align: center
      font-size: 1.1rem
      width: 2rem
      color: #fff
</style>
