<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="输入城市名或拼音">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    height: $headerHeight
    padding: 0 .4rem
    background: $bgColor
    .search-input
      box-sizing: border-box
      width: 100%
      height: 1.8rem
      padding: 0 .3rem
      text-align: center
      border-radius: .26rem
      background: #fff
      color: #ccc
      font-size: .9rem
</style>
