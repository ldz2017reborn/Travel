<template>
  <div>
    <div class="banner" @click="handleGalleryShow">
      <img class="banner-img" :src="bannerImg">
      <div class="banner-info">
        <div class="banner-title">{{sightName}}</div>
        <div class="banner-number">
          <span class="banner-icon iconfont">&#xe63c;</span>
          39
        </div>
      </div>
    </div>
    <fadeAnimation>
      <banner-gallery 
        v-show="show"
        @close="handleGalleryClose"
        :gallaryImgs="gallaryImgs"
      >        
      </banner-gallery>      
    </fadeAnimation>
  </div>
</template>

<script>
import BannerGallery from 'common/gallery/Gallery'
import fadeAnimation from 'common/fade/fadeAnimation'
export default {
  name: 'DetailBanner',
  props: {
    sightName: {
      type: String
    },
    bannerImg: {
      type: String
    },
    gallaryImgs: {
      type: Array
    }
  },
  components: {
    BannerGallery,
    fadeAnimation
  },
  data () {
    return {
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
