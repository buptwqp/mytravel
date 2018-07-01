<template>
  <div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of sweiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl"/>
    </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
  export default {
    name: 'carrousel',
    data() {
      return {
        swiperOption: {
          pagination: '.swiper-pagination',
          loop: true
        },
        sweiperList:[{
          id:'001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/22/0e335ab3af3e3f02.jpg_750x200_cf284e05.jpg'
        },{
          id:'002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1806/a1/e645466a5a1c9a02.jpg_750x200_9c489fbd.jpg'
        }]
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
