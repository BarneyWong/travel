<template>
  <div>
    <div class="recommend-title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList " v-bind:key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src='item.imgUrl'/>
        </div>
        <div class="item-info">
          <p class="item-title">{{ item.title }}</p>
          <p class="item-desc">{{ item.desc }}</p>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data: function () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg',
          title: '三亚自助游2222222222222ddddddddddddddddddddddddd',
          desc: '三亚三日自助游222222222'
        },
        {
          id: '0002',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg',
          title: '三亚自助游2222222222222ddddddddddddddddddddddddd',
          desc: '三亚三日自助游222222222'
        },
        {
          id: '0003',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg',
          title: '三亚自助游2222222222222ddddddddddddddddddddddddd',
          desc: '三亚三日自助游222222222'
        },
        {
          id: '0004',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg',
          title: '三亚自助游2222222222222ddddddddddddddddddddddddd',
          desc: '三亚三日自助游222222222'
        },
        {
          id: '0005',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg',
          title: '三亚自助游2222222222222ddddddddddddddddddddddddd',
          desc: '三亚三日自助游222222222'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~stylesdir/mixins.styl'
.recommend-title
  margin-top .2rem
  line-height .8rem
  background #eee
  text-indent .2rem
.item-img-wrapper
  overflow hidden
  height 0
  padding-bottom 44.3%
  .item-img
    width 100%
.item-info
  padding .1rem

  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()

  .item-desc
    line-height: .4rem
    color #ccc
    ellipsis()

</style>
