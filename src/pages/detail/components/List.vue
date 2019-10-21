<template>
  <div>
    <div class="item" v-for="(item,index) of list" :key="index">
      <div class="item-title">
        <span class="item-title-icon"></span>
        {{item.title}}
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :list="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  .item-title-icon
    // position: relative;
    display: inline-block
    // left: .2rem
    // top: .2rem
    width: .8rem;
    height: .8rem
    line-height: .8rem
    background: url('http://s.qunarzz.com/piao/image/touch/sight/detail.png') 0 -.55rem no-repeat;
    margin-right: .1rem;
    background-size: 1rem 5rem;
  .item-title
    line-height: 2.2rem
    font-size: .8rem
    padding: 0 .5rem
    border-bottom: .04rem solid #ccc
  .item-children
    padding: 0 1rem
</style>
