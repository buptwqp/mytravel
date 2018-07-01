<template>
  <div>
    <city-header>城市选择</city-header>
    <city-search></city-search>
  </div>

</template>

<script>
  import CityHeader from './commponents/Header'
  import CitySearch from './commponents/Search'
    export default {
        name: "City",
        components : {
          CitySearch,
          CityHeader
        }

    }
</script>

<style scoped>

</style>
