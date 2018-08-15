<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont">&#xe624;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{city}}
      <span class="iconfont arrow-icon">&#xe600;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}

</script>

<style lang="stylus" scoped>
    @import '~styles/variables.styl'
    .header
      display: flex
      line-height: .86rem
      background: $bgColor
      color: #fff
      .header-left
        width: .64rem
        float: left
        text-align: center
      .header-input
        flex: 1
        margin-top: .12rem
        margin-left: .2rem
        height: .62rem
        line-height: .62rem
        background: #fff
        color: #ccc
        border-radius: .1rem
        padding-left: .2rem
      .header-right
        width: 1.24rem
        float: right
        text-align: center
        .arrow-icon
          margin-left: -.06rem
          font-size: .24rem
</style>
