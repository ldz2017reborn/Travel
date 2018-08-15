<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>

</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫海洋主题乐园'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_150x150_06cb3e52.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫海洋主题乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/mixins.styl'
  .title
    height: .6rem
    line-height: .6rem
    background: #eee
    margin-top: .2rem
    padding-left: .1rem
  .item
    display: flex
    height: 1.9rem
    .item-img
      height: 1.7rem
      width: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
         line-height: .54rem
         font-size: .32rem
         ellipsis()
      .item-desc
        line-height: .4rem
        margin-top: 0.1rem
        color: #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .3rem
        padding 0 .2rem
        background: #ff9300
        color: #fff
        border-radius: .1rem
</style>
