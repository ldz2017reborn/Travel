<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe600;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState, mapGetters } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city']),
    ...mapGetters(['doubleCity'])
  }
}
</script>

<style lang="stylus" scoped>
    @import '~styles/variables.styl'
    .header
      display: flex
      line-height: $headerHeight
      background: $bgColor
      color: #fff
      .header-left
        width: .64rem
        float: left
        text-align: center
        .back-icon
          text-align: center
          font-size: .4rem
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
        min-width: 1.04rem
        padding: 0 .1rem
        float: right
        text-align: center
        color: #fff
        .arrow-icon
          margin-left: -.06rem
          font-size: .24rem
</style>
