<template>
  <div>
    <router-link to="/" tag="div" class="header-abs" v-show="showAbs">
      <div class="iconfont back-abs-icon">&#xe624;</div>
    </router-link>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
      城市选择
      <router-link to='/'>
        <div class="iconfont header-fixed-back">&#xe624;</div>
      </router-link>
    </div>
  </div>

</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header-abs
    position: fixed
    top: .2rem
    left: .2rem
    width: .8rem
    height: .8rem
    text-align: center
    line-height: .8rem
    border-radius: .4rem
    background: rgba(0, 0, 0, 0.8)
    .back-abs-icon
      color: #fff
      font-size: .4rem
  .header-fixed
    position: fixed
    left: 0
    right: 0
    top: 0
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    font-size: .32rem
    text-align: center
    color: #fff
    .header-fixed-back
      position: fixed
      text-align: center
      width: .64rem
      font-size: .4rem
      top: 0
      left: 0
      color: #fff
</style>
