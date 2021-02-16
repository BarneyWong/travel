<template>
  <div class="icons">
    <swiper :options="swiperOptions">
      <swiper-slide v-for="(page,index) of pages" v-bind:key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content"
                 :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{ item.desc }}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'icons',
  data: function () {
    return {
      swiperOptions: {},
      iconList: [
        {
          id: '0001',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游1'
        }, {
          id: '0002',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游222222222222'
        }, {
          id: '0003',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游3'
        }, {
          id: '0004',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游4'
        }, {
          id: '0005',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游5'
        }, {
          id: '0006',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游6'
        }, {
          id: '0007',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游7'
        }, {
          id: '0008',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游8'
        }, {
          id: '0009',
          imgUrl: 'https://pages.c-ctrip.com/groupTravelUED/travel_homepage/8.1.2icon/%E8%B7%9F%E5%9B%A2%E6%B8%B8.png',
          desc: '周边游9'
        }
      ]
    }
  },
  computed: {
    pages: function () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })

      return pages
    }
  }

}
</script>

<style lang="stylus" scoped>
@import '~stylesdir/varibles.styl'
@import '~stylesdir/mixins.styl'
.icons >>> .swiper-container
  height 0
  padding-bottom 50%

.icon
  position relative
  overflow hidden
  float left
  width 25%
  height 0
  padding-bottom 25%

  .icon-img
    position absolute
    top 0
    left 0
    right 0
    bottom .44rem
    box-sizing border-box
    padding .1rem

    .icon-img-content
      height 100%
      display block
      margin 0 auto

  .icon-desc
    position: absolute
    left 0
    right 0
    bottom 0
    height .44rem
    line-height .44rem
    //background $bgColor
    text-align center
    ellipsis()

</style>
