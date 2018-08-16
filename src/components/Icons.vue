<template>
    <div class="icons">
        <swiper :options="swiperOption">
            <swiper-slide v-for= "(page, index) in pages" :key="index">
                <div class="icon"
                     v-for="(item, index) in page"
                     :key="item.id"
                >
                    <div class="icon-img" :class="'icon-img-bg' + index">
                        <img class="icon-img-content" :src="item.imgUrl" alt="">
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
    export default {
        name: "HomeIcons",
        data () {
            return {
                swiperOption: {},
                bgcolor: ["red","green","yellow"],
                iconList: [
                    {
                        id: "001",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png",
                        desc: "海外玩乐",
                    },  {
                        id: "002",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/trans_machine.png",
                        desc: "旅行装备"
                    },  {
                        id: "003",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png",
                        desc: "海外玩乐"
                    },  {
                        id: "004",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/trans_machine.png",
                        desc: "旅行装备"
                    },  {
                        id: "005",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png",
                        desc: "海外玩乐"
                    },  {
                        id: "006",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/trans_machine.png",
                        desc: "旅行装备"
                    },  {
                        id: "007",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png",
                        desc: "海外玩乐"
                    },  {
                        id: "008",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/trans_machine.png",
                        desc: "旅行装备"
                    },  {
                        id: "009",
                        imgUrl: "https://s.qunarzz.com/package_mobile/app/outbround/play_v2.png",
                        desc: "海外玩乐"
                    }
                ]
            }
        },
        computed: {
            pages () {
                const pages = [];
                this.iconList.forEach((item, index) => {
                    const page = Math.floor(index / 8);
                    if(!pages[page]){
                        pages[page] = [];
                    }
                    pages[page].push(item);
                })
                return pages
            }
        }
    }
</script>

<style lang="stylus" scoped>
    @import"~styles/varibles.styl"
    @import"~styles/mixins.styl"
    .icons >>> .swiper-container
      height:0
      padding-bottom: 50%
    .icons
      overflow: hidden;
      width: 100%
      height:0
      padding-bottom: 50%
      .icon
        position: relative
        overflow: hidden
        float: left
        width: 25%
        height: 0
        padding-bottom: 25%
        .icon-img
          position: relative
          overflow: hidden
          display: inline-block
          width: 1.1rem
          height: 1.1rem
          border-radius: .4rem
          margin-top: .24rem
          .icon-img-content
            position: absolute
            top: 0
            left: 0
            bottom: 0
            right: 0
            display: block
            width: 1.1rem;
            height: 1.1rem;
        .icon-desc
          position: absolute
          left: 0
          bottom: .16rem
          right: 0
          height: .44rem
          line-height: .44rem
          color: $darkTextColor
          ellipse()
      .icon-img-bg0
        background: #f9a62c;
        background: -moz-linear-gradient(-180deg,#f9a62c 0,#fe6a39 100%);
        background: -webkit-linear-gradient(-180deg,#f9a62c 0,#fe6a39 100%);
        background: linear-gradient(-180deg,#f9a62c 0,#fe6a39 100%);
      .icon-img-bg1
        background: #f67be1;
        background: -moz-linear-gradient(-180deg,#f67be1 0,#aa5cff 100%);
        background: -webkit-linear-gradient(-180deg,#f67be1 0,#aa5cff 100%);
        background: linear-gradient(-180deg,#f67be1 0,#aa5cff 100%);
      .icon-img-bg2
        background: #fa69da;
        background: -moz-linear-gradient(-180deg,#fa69da 0,#ea40a5 100%);
        background: -webkit-linear-gradient(-180deg,#fa69da 0,#ea40a5 100%);
        background: linear-gradient(-180deg,#fa69da 0,#ea40a5 100%);
      .icon-img-bg3
        background: #13deff;
        background: -moz-linear-gradient(-180deg,#13deff 0,#039bff 100%);
        background: -webkit-linear-gradient(-180deg,#13deff 0,#039bff 100%);
        background: linear-gradient(-180deg,#13deff 0,#039bff 100%);
      .icon-img-bg4
        background: #44b8fb;
        background: -moz-linear-gradient(-180deg,#44b8fb 0,#6d68df 100%);
        background: -webkit-linear-gradient(-180deg,#44b8fb 0,#6d68df 100%);
        background: linear-gradient(-180deg,#44b8fb 0,#6d68df 100%);
      .icon-img-bg5
        background: #fccd37;
        background: -moz-linear-gradient(-180deg,#fccd37 0,#fb9f0b 100%);
        background: -webkit-linear-gradient(-180deg,#fccd37 0,#fb9f0b 100%);
        background: linear-gradient(-180deg,#fccd37 0,#fb9f0b 100%);
      .icon-img-bg6
        background: #aff13a;
        background: -moz-linear-gradient(-180deg,#aff13a 0,#51cf1f 100%);
        background: -webkit-linear-gradient(-180deg,#aff13a 0,#51cf1f 100%);
        background: linear-gradient(-180deg,#aff13a 0,#51cf1f 100%);
    .icon-img-bg7
        background: #fc8762;
        background: -moz-linear-gradient(-180deg,#fc8762 0,#f92d73 100%);
        background: -webkit-linear-gradient(-180deg,#fc8762 0,#f92d73 100%);
        background: linear-gradient(-180deg,#fc8762 0,#f92d73 100%);
</style>