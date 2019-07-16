<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper" v-for="item of hot" :key="item.id">
            <div class="button">{{item.name}}</div>
          </div>
        </div>
      </div>
      <div class="area" v-for="(item, key) of cities" :key="key">
        <div class="title">{{key}}</div>
        <div class="item-list">
          <div class="item border-bottom" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    hot: Array,
    cities: Object
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
@import '~styles/mixins.styl'
.list
  position: absolute
  overflow: hidden
  top: 5.2rem
  left: 0
  right: 0
  bottom: 0
  .title
    title-common()
  .button-list
    overflow: hidden
    padding: .4rem 2.2rem .4rem .4rem
    .button-wrapper
      width: 33.3%
      text-align: center
      float: left
      .button
        font-size: 1.2rem
        margin: .3rem
        padding: .2rem 0
        text-align: center
        border: .04rem solid #ccc
        border-radius: .3rem
  .item-list
    .item
      line-height: 2.2rem
      padding-left: .8rem
    .border-bottom
      &:before
        border-color: #ccc
</style>
