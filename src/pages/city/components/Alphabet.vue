<template>
  <ul class="list">
    <li class="item" v-for="(item, key) of cities" :key="key" @click="handleLetterClick" @touchStart="handleTouchStart" @touchMove="handleTouchMove" @touchEnd="handleTouchEnd">
      {{key}}
    </li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  data () {
    return {
      touchStatus: false
    } 
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    },
    handleTouchStart () {
      this.touchStatus = true
    },
    handleTouchMove () {

    },
    handleTouchEnd () {
      this.touchStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list
    display: flex
    flex-direction: column
    justify-content: center
    position: absolute
    top: 5.2rem
    right: 0
    bottom: 0
    width: 1.2rem
    color: $bgColor
    .item
      text-align: center
      line-height: 1.6rem
</style>
