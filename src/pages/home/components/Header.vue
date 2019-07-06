<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont arrow">&#xe6aa;</span>
    </div>
  </div>
</template>
<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    line-height: 2.6rem
    display: flex
    background-color: $bgColor
    color #fff
    font-size: .9rem
    .header-left
      min-width: 2rem
      float: left
      .back-icon
        text-align: center
        font-size: 1rem
    .header-input
      flex: 1
      margin-top: .3rem
      height: 1.9rem
      line-height: 1.9rem
      margin-left: .2rem
      margin-right: .4rem
      padding-left: .4rem
      background: #fff
      color: #ccc
      border-radius: .2rem
    .header-right
      min-width: 3.26rem
      float: right
      .arrow
        font-size: .4rem
</style>
