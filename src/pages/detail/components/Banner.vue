<template>
  <div>
    <div class="banner" @click="handleGalleryShow">
      <img class="banner-img" src="//img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_600x330_bf9c4904.jpg">
      <div class="banner-info">
        <div class="banner-title">大连圣亚海洋世界(AAAA景区)</div>
        <div class="banner-number">
          <span class="banner-icon iconfont">&#xe63c;</span>
          39
        </div>
      </div>
    </div>
    <banner-gallery :imgs1="imgs" v-show="show" @close="handleGalleryClose"></banner-gallery>
  </div>
</template>

<script>
import BannerGallery from 'common/gallery/Gallery'
export default {
  name: 'DetailBanner',
  components: {
    BannerGallery
  },
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1602/39/39f6b1003abe1b2790.img.jpg_350x240_fc004ff3.jpg', 'http://img1.qunarzz.com/sight/p0/1807/7d/7d64de6b134d10eaa3.img.jpg_350x240_3f1621ed.jpg'],
      show: false
    }
  },
  methods: {
    handleGalleryShow () {
      this.show = true
    },
    handleGalleryClose () {
      this.show = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      right: 0
      left: 0
      bottom: 0
      line-height: .6rem
      color: #fff
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        font-size: .32rem
        padding: 0 .2rem
      .banner-number
        line-height: .32rem
        height: .32rem
        padding: 0 .4rem
        margin-top: .14rem
        border-radius: .2rem
        font-size: .24rem
        background: rgba(0, 0, 0, 0.8)
        .banner-icon
          font-size: .24rem
</style>
