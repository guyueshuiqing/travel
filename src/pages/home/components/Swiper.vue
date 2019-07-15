<template>
  <div class="swiper">
    <swiper :options="swiperOption" v-if="showSiwper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSiwper () {
      return this.list.length
    }
  }
}
</script>
<style lang="stylus" scoped>
.swiper >>> .swiper-pagination-bullet-active
  background: #fff
.swiper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 26.66%
  .swiper-img
    width: 100%
</style>
