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
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
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
  @import '~styles/varibles.styl'
  .header
    display flex
    line-height $headerHeight
    background $bgColor
    color #fff
    box-shadow 0 2px 13px 5px rgba(0, 0, 0, 0.02)
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      height .62rem
      line-height .62rem
      margin .12rem
      margin-left .2rem
      background #fff
      border-radius .1rem
      color #e2e2e2
      padding-left .2rem
    .header-right
      width 1.24rem
      float right
      text-align center
      color #fff
      .arrow-icon
      margin-left -.  04rem
        font-size .3rem

</style>
