<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe685;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe67d;</span>输入城市/游玩主题
    </div>
    <div class="header-right ">
      {{ this.city }}<span class="iconfont">&#xe688;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import '~stylesdir/varibles.styl'
  .header
    display flex
    line-height.86rem
    background $bgColor
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      padding-left .2rem
      height .64rem
      line-height .64rem
      margin-top .12rem
      margin-bottom .12rem
      background #fff
      border-radius 0.1rem
      color #ccc
    .header-right
      width 1.24rem
      float right
      text-align center
</style>
