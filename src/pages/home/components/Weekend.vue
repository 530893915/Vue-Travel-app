<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1509/ff/4184c6c13edbb.jpg_r_640x214_60474b61.jpg',
          title: '成都周边秋色',
          desc: '细数成都周边秋天最美仙境'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1509/ff/4184c6c13edbb.jpg_r_640x214_60474b61.jpg',
          title: '成都周边秋色',
          desc: '细数成都周边秋天最美仙境'
        },
        {
          id: '0003',
          imgUrl: 'http://img1.qunarzz.com/sight/source/1509/ff/4184c6c13edbb.jpg_r_640x214_60474b61.jpg',
          title: '成都周边秋色',
          desc: '细数成都周边秋天最美仙境'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      font-weight bold
      ellipsis()
    .item-desc
      line-height .4rem
      color #565656
      font-size .2rem
      ellipsis()
</style>
