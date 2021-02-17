<template>
  <div class="header">
    <router-link to="/">
      <div class="header-back iconfont">&#xe685;</div>
    </router-link>
    请选择城市
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~stylesdir/varibles.styl'
  .header
    position relative
    overflow hidden
    height $headerHeight
    line-height $headerHeight
    text-align center
    color #fff
    background $bgColor
    font-size .32rem
    .header-back
      position: absolute;
      width .64rem
      text-align center
      font-size .4rem
      color #fff
</style>
