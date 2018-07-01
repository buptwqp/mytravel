<template>
 <div>
   <div class="recommend-title">热销推荐</div>
   <ul>
     <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
       <img class="item-img" :src="item.imgUrl"/>
       <div class="item-info">
         <p class="item-title">{{item.title}}</p>
         <p class="item-desc">{{item.desc}}</p>
         <button class="item-button">查看详情</button>
       </div>
     </li>
   </ul>
 </div>
</template>

<script>
    export default {
        name: "Recommend",
        data () {
        return {
          recommendList:[{
            id:'001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/a3/a3924161475dee37a3.img.jpg_200x200_5ba00364.jpg',
            title:'青岛海昌极地海洋世界elliosis',
            desc:'青岛海昌极地海洋世界'
          },{
            id:'002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/a3/a3924161475dee37a3.img.jpg_200x200_5ba00364.jpg',
            title:'青岛海昌极地海洋世界elliosis',
            desc:'青岛海昌极地海洋世界'
          },{
            id:'003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/a3/a3924161475dee37a3.img.jpg_200x200_5ba00364.jpg',
            title:'青岛海昌极地海洋世界elliosis',
            desc:'青岛海昌极地海洋世界'
          },{
            id:'004',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1707/a3/a3924161475dee37a3.img.jpg_200x200_5ba00364.jpg',
            title:'青岛海昌极地海洋世界elliosis',
            desc:'青岛海昌极地海洋世界'
          },]

        }
      }
    }

</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .recommend-title
    margin-top .2rem
    line-height .8rem
    background-color #eee
    text-align left
    text-indent .2rem
  .item
    text-align left
    overflow hidden
    display flex
    height 1.9rem
    /*background-color red*/
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        elliosis()
      .item-desc
        line-height .4rem
        color #ccc
        elliosis()
      .item-button
        line-height .44rem
        margin-top .16rem
        background-color #ff9300
        padding 0.1rem
        border-radius .06rem

</style>
