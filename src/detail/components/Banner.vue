<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1807/ad/ad574bfe6c9e1ceda3.img.png_600x330_0046c90a.png" alt="">
      <div class="banner-info">
        <div class="banner-tittle">
          成都欢乐谷
        </div>
        <div class="banner-numble"><span class="iconfont arrow-icon">&#xe60f;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary"
    @close="handleGallaryClose"
    >
    </common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallary: false,
      imgs: [
        'http://img1.qunarzz.com/sight/p0/1712/5d/5d4f18e64813d0f6a3.img.jpg_350x240_3148867f.jpg',
        'http://img1.qunarzz.com/sight/p0/1509/79/4617b478f24f03b7b2ad5e73fbd06740.water.jpg_350x240_a0176ff6.jpg'
      ]
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  },
  components: {
    CommonGallary
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0
      line-height .6rem
      color #fff
      background-image linear-gradient(top, rgba(0,0,0,0), rgba(0,0,0, 0.8))
      .banner-tittle
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-numble
        height 0.32rem
        line-height .32rem
        margin-top .14rem
        padding 0 .4rem
        border-radius .2rem
        background rgba(0,0,0, .8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
