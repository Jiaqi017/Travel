<template>
    <div class="search">
        <input class="input-search" type="text" placeholder="添加城市名或拼音"/>
    </div>
</template>
<script>
    export default {
        name: 'CitySearch'
    }
</script>

<style lang="stylus" scoped>
    @import "~styles/varibles.styl"
    .search
      padding: 0 .1rem
      height: .72rem
      background: $bgcolor
      .input-search
        padding: 0 .1rem
        box-sizing: border-box
        width: 100%
        height: .62rem
        border-radius: .06rem
        text-align: center
        background: #ffffff
        color: #666
</style>