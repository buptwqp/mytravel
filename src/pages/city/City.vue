<template>
  <div>
    <city-header>城市选择</city-header>
    <city-search></city-search>
    <city-list></city-list>
    <city-alphabet></city-alphabet>
  </div>

</template>

<script>
  import CityHeader from './commponents/Header'
  import CitySearch from './commponents/Search'
  import CityList from './commponents/List'
  import CityAlphabet from  './commponents/Alphabet'
    export default {
        name: "City",
        components : {
          CitySearch,
          CityHeader,
          CityList,
          CityAlphabet
        }

    }
</script>

<style lang="stylus" scoped>
  .list
    position absolute
    right 0
    top 1.58rem
    bottom 0
    width .4rem
</style>
