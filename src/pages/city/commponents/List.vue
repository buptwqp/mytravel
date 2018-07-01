<template>
  <div class="list" ref='wrapper'>
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>

      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper" v-for="item of hot" :key="item.id">
            <div class="button">{{item.name}}</div>
          </div>

        </div>
      </div>

      <div class="area" v-for="(item,key) of cities" :key="key">
        <div class="title border-topbottom">{{key}}</div>
        <div class="item-list" v-for="innerItem of item" :key="item.id">
          <div class="item border-bottom">{{innerItem.name}}</div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  import BScroll from 'better-scroll'
  export default {
    name: "List",
    props: {
      hot : Array,
      cities: Object
    },
    mounted () {
      this.scroll=new BScroll(this.$refs.wrapper)
    }
  }
</script>

<style lang="stylus" scoped>
  .border-topbottom
    &:befoer
      border-color #ccc
    &:after
      border-color #ccc

  .border-bottom
    &:befoer
      border-color #ccc

  .list
    position absolute
    overflow hidden
    top 1.52rem
    left 0
    right 0
    bottom 0
    width 100%
    .title
      text-align left
      line-height .44rem
      background #eee
      padding-left .26rem
      color #666
    .button-list
      padding .1rem
      overflow hidden
      padding .1rem .6rem .1rem
      .button-wrapper
        width 33.33%
        float left
        .button
          margin .1rem
          text-align center
          border .02rem solid #ccc
    .item-list
      text-align left
      .item
        line-height .76rem
        color #666
        padding-left .2rem
</style>
