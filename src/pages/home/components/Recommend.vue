<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul>
      <router-link :to="'/detail/' + item.id" tag="li" class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </router-link>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .4rem
    title-common()
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
