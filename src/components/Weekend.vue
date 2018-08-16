<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" alt="" class="item-img">
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
        name: "HomeWeekend",
        data () {
            return {
                recommendList: [
                    {
                        id: '0001',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0002',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0003',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0004',
                        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/68/de862f94e383a6.jpg_r_640x214_f9df927b.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    }
                ]
            }
        }
    }
</script>
<style lang="stylus" scoped>
    @import '~styles/mixins.styl'
    .title
      margin-top: .2rem
      line-height: .8rem
      background: #eee
      text-align: left
      text-indent: .2rem
    .item-img-wrapper
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 33.9%
      .item-img
        width: 100%
    .item-info
        padding: .1rem
        text-align: left
        .item-title
            line-height: .54rem
            font-size: .32rem
            ellipse()
        .item-desc
            line-height: .4rem
            ellipse()
            color: #ccc

</style>
















