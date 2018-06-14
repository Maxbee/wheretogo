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
export default {
  name: "Home",
  components: {
    Header,
    Swiper,
    Icons
  }
};
</script>
<style lang="stylus" scope>
</style>
