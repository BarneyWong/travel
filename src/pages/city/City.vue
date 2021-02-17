<template>
  <div>
    <city-header></city-header>
    <city-search></city-search>
    <city-list></city-list>
  </div>
</template>

<script>
import CityHeader from './components/CityHeader'
import CitySearch from './components/CitySearch'
import CityList from './components/CityList'
export default {
  name: 'City',
  components: {
    CityHeader: CityHeader,
    CitySearch: CitySearch,
    CityList: CityList
  }
}
</script>

<style lang="stylus" scoped>

</style>
