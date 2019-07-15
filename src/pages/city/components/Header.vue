<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position: relative
    overflow: hidden
    height: $headerHeight
    line-height: $headerHeight
    font-size: 1rem
    text-align: center
    color: #fff
    background: $bgColor
    .header-back
      position: absolute
      left: 0
      top: 0
      text-align: center
      font-size: 1rem
      width: 2rem
      color: #fff
</style>
