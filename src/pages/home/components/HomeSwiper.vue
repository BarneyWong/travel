<template>
  <div class="wrapper">
    <swiper  :options="swiperOptions">
      <swiper-slide v-for="item of swiperList" v-bind:key="item.id">
        <img class="swiper-img" v-bind:src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOptions: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg'
        },
        {
          id: '0002',
          imgUrl: 'https://dimg04.c-ctrip.com/images/0zg2i120008a7304uC5C6.jpg'
        }
      ]
    }
  }
}

</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background red !important

.wrapper
  overflow hidden
  width 100%
  height 0
  padding-bottom 31.25%

  .swiper-img
    width 100%
</style>
