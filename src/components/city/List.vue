<template>
    <div class="list" ref="wrap">
        <div>
            <div class="area">
                <div class="title border-topbottom">当前城市</div>
                <div class="button-list">
                    <div class="button-wrapper" v-for="item of hot" :key="item.id">
                        <div class="button">{{item.name}}</div>
                    </div>

                </div>
            </div>
            <div class="area" v-for="(item, key) of cities" :key="key">
                <div class="title border-topbottom">{{key}}</div>
                <div class="item-list">
                    <div class="item border-bottom" v-for="innerItem of item" :key="innerItem.id">{{innerItem.name}}</div>

                </div>

            </div>

        </div>

    </div>
</template>
<script>
    import Bscroll from 'better-scroll'
    export default {
        name: 'CityList',
        props: {
            cities: Object,
            hot: Array
        },
        mounted () {
            this.scroll = new Bscroll(this.$refs.wrap);
        }
    }
</script>

<style lang="stylus" scoped>
    @import "~styles/varibles.styl"
    .border-topbottom
      &:before
        border-color: #777
      &:after
        border-color: #777
    .border-bottom
      &:before
        border-color: #777
    .list
      position: absolute
      top: 1.58rem
      right: 0
      bottom: 0
      left: 0
      overflow: hidden
      .title
        padding-left: .2rem
        height: .54rem
        line-height: .54rem
        background: #eee
        color: #666
        font-size: .26rem
        text-align: left
      .button-list
        padding: .1rem .6rem .1rem .1rem
        overflow: hidden
        .button-wrapper
          float: left
          width: 33.3%
          .button
            margin: .1rem
            padding: .1rem 0
            border: .02rem solid #ccc
      .item-list
        .item
          padding-left: .2rem
          line-height: .76rem
          color: #666
          text-align: left



</style>