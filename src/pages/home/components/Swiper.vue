<template>
  <div class="wrapper">
    <swiper :options="swiperOption" >
        <swiper-slide v-for="item of swiperList" :key="item.id">
            <img class="swiper-img" :src="item.imgURL" alt="">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data: function () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000,
        autoplayDisableOnInteraction: false
      },
      swiperList: [{
        id: '0001',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1806/e5/fc2bfc8bfcccd402.jpg_750x200_1218ab5f.jpg'
      },
      {
        id: '0002',
        imgURL: 'http://img1.qunarzz.com/piao/fusion/1811/b4/ac00a771d74f5a02.jpg_750x200_a71cff60.jpg'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  // overflow: hidden
  width: 100%
  height: 31.25vm
  // height:0
  // padding-bottom: 31.25%
  .swiper-img
    width: 100%
</style>
