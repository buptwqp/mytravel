<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont ">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入游玩城市/景点/游玩主题</div>
    <div class="header-right">
       {{this.city}}
      <span class="iconfont">&#xe695;</span>
    </div>
  </div>

</template>

<script>
    export default {
        name: "Header",
        props : {
          city: String

        }
    }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    background-color $bgColor;
    line-height .86rem
    display flex
    height .86rem
    color #fff
    .header-left
      width .64rem
      float left
    .header-input
      flex:1
      height : .64rem
      line-height : .64rem
      margin-top: .12rem
      background-color: #fff;
      border-radius: .1rem
      color :#ccc

    .header-right
      width:1.24rem
      float:rigth
      text-align: center

</style>
