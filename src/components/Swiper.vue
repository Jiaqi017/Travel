<template>
    <div class="wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class='swiper-img' :src="item.imgUrl"/>
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination" slot="pagination"></div>

        </swiper>
    </div>

</template>

<script>
    export default {
        name: 'HomeSwiper',
        data () {
            return {
                swiperOption: {
                    pagination: ".swiper-pagination",
                    loop: true

                },
                swiperList: [
                    {
                        id: "0001",
                        imgUrl: "https://imgs.qunarzz.com/vc/c4/38/76/284d1c5cd02b88a4cd7247b8e3.jpg_92.jpg"
                    },{
                        id: "0002",
                        imgUrl: "https://imgs.qunarzz.com/ftejia/1807/73/0d47b847a6d675.jpg"
                    },{
                        id: "0003",
                        imgUrl: "https://imgs.qunarzz.com/vc/89/19/e9/ff75c13186670f36111d2e5640.jpg_92.jpg"
                    }
                ]
            }
        }
    }
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
    .wrapper
      overflow: hidden;
      width: 100%
      height: 0
      padding-bottom: 51.73%
      background: #eee
    .swiper-img
      width: 100%
</style>