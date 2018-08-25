<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe749;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe86e;</span>
            输入城市景点/景点
        </div>
        <router-link to="/city">
            <div class="header-right">
                城市
                <span class="iconfont arrow-icon">&#xe64a;</span>
            </div>
        </router-link>
    </div>
</template>

<style lang="stylus" scoped>
    @import "~styles/varibles.styl"
    .header
      display: flex
      line-height: .86rem
      background: $bgcolor
      color: #fff
      .header-left
        width: .64rem
        float: left
        .back-icon
          font-size: .4rem
          text-align: center
      .header-input
        flex: 1
        height: .64rem
        line-height: .64rem
        margin-left: .2rem
        margin-top: .12rem
        padding-left: .2rem
        background: #fff
        border-radius: .1rem
        color: #ccc
        text-align: left
      .header-right
        width: 1.24rem
        float: right
        color: #fff
        .arrow-icon
          font-size: .24rem


</style>