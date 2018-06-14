<template>
<div>
    <Header></Header>
    <Swiper></Swiper>
    <Icons></Icons>
</div>
</template>
<script>
import Header from "./components/Header"
import Swiper from './components/HomeSwiper'
import Icons from './components/Icon'
import axios from 'axios'
export default {
  name: "Home",
  components: {
    Header,
    Swiper,
    Icons
  },
  methods:{
      getData(res){
          console.log(res)
      }
  },
  mounted () {
      axios.get('/static/mock/index.json').then(this.getData)
  }
};
</script>
<style lang="stylus" scope>
</style>
