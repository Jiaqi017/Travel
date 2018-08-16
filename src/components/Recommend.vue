<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item in recommendList" :key="item.id">

                <img :src="item.imgUrl" alt="" class="item-img">

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
        name: "HomeRecommend",
        data () {
            return {
                recommendList: [
                    {
                        id: '0001',
                        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0002',
                        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0003',
                        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg',
                        title: '白水洋',
                        desc: '白水洋白水洋白水洋'
                    },{
                        id: '0004',
                        imgUrl: 'http://img1.qunarzz.com/sight/p0/1707/45/4524631d448c1aea3.water.jpg_200x200_b7b204e1.jpg',
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
  .item
    text-align: left
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipse()
      .item-desc
        line-height: .4rem
        ellipse()
        color: #ccc
      .item-button
        margin-top: .16rem
        line-height: .44rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
















