<template>
  <div class="home">
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    <home-weekend></home-weekend>
  </div>
</template>

<script>
// @ is an alias to /src

import HomeHeader from "@/components/Header.vue";
import HomeSwiper from "@/components/Swiper.vue";
import HomeIcons from "@/components/Icons.vue";
import HomeRecommend from "@/components/Recommend.vue";
import HomeWeekend from "@/components/Weekend.vue";
import axios from "axios"
export default {
  name: "Home",
  components: {
    HomeHeader: HomeHeader,
    HomeSwiper,
    HomeIcons,
    HomeRecommend,
    HomeWeekend
  },
  methods: {
      getHomeInfo () {
          axios.get('/static/resource/index.json')
              .then(this.getHomeInfoSucc)
      },
      getHomeInfoSucc (res) {
          console.log(res)
      }

  },
  mounted () {
      this.getHomeInfo()
  }

};
</script>
