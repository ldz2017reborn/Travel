<template>
  <div class="search">
    <input class="input-search" type="text" placeholder="请输入城市名字" />
  </div>
</template>

<script>
export default {
  name: 'HomeSearch'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variables.styl'
  .search
    height: .72rem
    padding: 0 .1rem
    background: $bgColor
    .input-search
      box-sizing: border-box
      width: 100%
      height: .62rem
      line-height: .62rem
      border-radius: .06rem
      text-align: center
      padding: 0.1rem
</style>
