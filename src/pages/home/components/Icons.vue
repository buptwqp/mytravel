<template>
  <div class="icons">

    <swiper>
      <swiper-slide v-for="(page,index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.imgDesc}}</p>
        </div>
      </swiper-slide>
    </swiper>

  </div>

</template>

<script>
    export default {
        name: "HomeIcons",
        data(){
          return{
          iconList:[{
            id:'001',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点1111111111111'
          },{
            id:'002',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'003',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
            },{
            id:'004',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'005',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'006',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'007',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'008',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'热门景点'
          },{
            id:'009',
            imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
            imgDesc:'甘肃'
          }]
          }},
      computed: {
          pages () {
            const pages=[];
            this.iconList.forEach((item,index)=>{
              const page =Math.floor(index/8)
              if(!pages[page]){
                pages[page]=[];
              }
              pages[page].push(item);
            })
            return pages
          }


      }
    }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  @import "~styles/mixins.styl"
  .icons
    overflow hidden
    height 0
    padding-bottom 50%
    overflow  hidden
    /*background #1e16c9*/
    .icon
      position relative
      height  0
      float left
      width 25%
      padding-bottom 25%
      /*background-color #ccff95*/
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-sizing border-box
        padding .1rem
        /*background #fc2933*/
        .icon-img-content
          height 100%
          display block
          margin 0 auto
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        color $darkText
        elliosis()


</style>
