<template>
    <div>
        <city-header></city-header>
        <city-search></city-search>
        <city-list :cities="cities" :hot="hotCities"></city-list>
        <city-alphabet :cities="cities"></city-alphabet>
    </div>

</template>

<script>
    import CityHeader from '../components/city/Header.vue'
    import CitySearch from '../components/city/Search.vue'
    import CityList from '../components/city/List.vue'
    import CityAlphabet from '../components/city/Alphabet.vue'
    import axios from 'axios'
    export default {
        name: 'City',
        data () {
            return {
                cities: {},
                hotCities: []
            }
        },
        components: {
            CityHeader,
            CitySearch,
            CityList,
            CityAlphabet
        },
        methods: {
            getCityInfo () {
                axios.get('/static/resource/city.json')
                    .then(this.getCityInfoSucc)
            },
            getCityInfoSucc (res) {
                res = res.data;
                if(res.ret && res.data) {
                    const data = res.data;
                    this.cities = data.cities;
                    this.hotCities = data.hotCities;
                }
            }

        },
        mounted () {
            this.getCityInfo()
        }

    }
</script>

<style lang="stylus" scoped>

</style>
