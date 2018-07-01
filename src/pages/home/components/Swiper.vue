<template>
  <div class="wrapper">
  <swiper :options="swiperOption" v-if="list.length">
    <swiper-slide v-for="item of list" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl"/>
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
  export default {
    name: 'carrousel',
    props :{
      list: Array
    },
    data() {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop: true,
          autoplay:true
        }
      }
    }
  }
</script>
<style lang="stylus" scoped>
  .wrapper
    width 100%
    height 0
    overflow hidden
    padding-bottom 31%
    .swiper-img
      width 100%

</style>
