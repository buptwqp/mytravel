<template>
 <div>
   <div class="recommend-title">热销推荐</div>
   <ul>
     <li class="item border-bottom" v-for="item of list" :key="item.id">
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
        props:{
          list:Array
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
