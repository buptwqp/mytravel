<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入城市名或者拼音">
  </div>

</template>

<script>
    export default {
        name: "CitySearch"
    }
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .search
    padding 0 .1rem;
    height .72rem
    background-color $bgColor
    .search-input
      box-sizing border-box
      width 100%
      height .62rem
      line-height .62rem
      border-radius .06rem
      text-align center
      color #666
      padding 0 .6rem

</style>
