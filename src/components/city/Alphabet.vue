<template>
    <ul class="list">
        <li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>

    </ul>
</template>
<script>
    import Bscroll from 'better-scroll'
    export default {
        name: 'CityAlphabet',
        props: {
            cities: Object,
        }
    }
</script>

<style lang="stylus" scoped>
    @import "~styles/varibles.styl"
    .list
      display: flex
      flex-direction: column
      justify-content: center
      position: absolute
      top: 1.58rem
      right: 0
      bottom: 0
      width: .4rem
      .item
        line-height: .44rem
        color: $bgColor
</style>