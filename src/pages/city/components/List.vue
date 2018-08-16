<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title boder-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title boder-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
          <div class="button-wraper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title boder-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title boder-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title boder-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
          <div class="item border-bottom">阿拉尔</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .list
    overflow: hidden
    position: absolute
    left: 0
    right: 0
    top: 1.58rem
    bottom: 0
    .area
      .boder-topbottom
        border-top: .02rem solid #777
        border-bottom: .02rem solid #777
      .title
        line-height: .54rem
        background: #eee
        color: #666
        font-size: .26rem
        padding-left: .2rem
      .button-list
        overflow: hidden
        padding: .1rem .6rem .1rem .1rem
        .button-wraper
          float: left
          width: 33.33%
          .button
            margin: .1rem
            text-align: center
            border: .02rem solid #ccc
            padding: .1rem 0
            border-radius: .06rem
      .item-list
        .item
          line-height: .54rem
          padding-left: .2rem
</style>
