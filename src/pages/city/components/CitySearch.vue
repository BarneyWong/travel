<template>
  <div class="search">
    <input class="search-input" type="text" placeholder="输入关键词">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<style lang="stylus" scoped>
@import '~stylesdir/varibles.styl'
.search
  height .72rem
  padding 0 .1rem
  background $bgColor
  .search-input
    box-sizing border-box
    height .62rem
    line-height .62rem
    padding 0 .1rem
    width 100%
    text-align center
    border-radius .06rem
    color #666
</style>
