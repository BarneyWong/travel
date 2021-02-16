<template>
  <div>
    <Header></Header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
  </div>
</template>

<script>
import Header from './components/Header'
import HomeSwiper from './components/HomeSwiper'
import HomeIcons from './components/HomeIcons'
export default {
  name: 'Home',
  components: {
    Header: Header,
    HomeSwiper: HomeSwiper,
    HomeIcons: HomeIcons
  }
}
</script>
<style>
</style>
