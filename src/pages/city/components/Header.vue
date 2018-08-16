<template>
  <div class="header">
    城市选择
    <router-link to='/'>
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .header
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    font-size: .32rem
    text-align: center
    color: #fff
    .header-back
      position: absolute
      text-align: center
      width: .64rem
      font-size: .4rem
      top: 0
      left: 0
      color: #fff
</style>
