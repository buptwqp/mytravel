<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-warapper">
          <img class="item-img" :src="item.imgUrl"/>
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
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
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
          title:'青岛海昌极地海洋世界elliosis',
          desc:'青岛海昌极地海洋世界'
        },{
          id:'002',
          imgUrl:'http://img1.qunarzz.com/sight/source/1505/85/708da4ab8dba17.jpg_r_640x214_d3d8cfa5.jpg',
          title:'青岛海昌极地海洋世界elliosis',
          desc:'青岛海昌极地海洋世界'
        }]

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
 .item-img-warapper
    height 0
    overflow hidden
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      elliosis()
    .item-desc
      line-height .4rem
      color #ccc
      elliosis()



</style>
