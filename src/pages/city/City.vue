<template>
  <div>
    <city-header>城市选择</city-header>
    <city-search></city-search>
    <city-list :cities="cities" :hot="hotCities"></city-list>
    <city-alphabet :cities="cities"></city-alphabet>
  </div>

</template>

<script>
  import CityHeader from './commponents/Header'
  import CitySearch from './commponents/Search'
  import CityList from './commponents/List'
  import CityAlphabet from  './commponents/Alphabet'
  import axios from 'axios'
    export default {
        name: "City",
        components : {
          CitySearch,
          CityHeader,
          CityList,
          CityAlphabet
        },
      data () {
          return {
            cities:{},
            hotCities: []
          }
      },
        mounted() {
          this.getCityInfo()
        },
        methods:{
          getCityInfo (){
            axios.get('/api/city.json')
              .then(this.handleGetCityInfoSucc)
          },
          handleGetCityInfoSucc(res) {
            res=res.data;
            if(res.ret && res.data){
              console.log(res);
              const data=res.data;
              this.cities=data.cities;
              this.hotCities=data.hotCities;

            }
          }

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
