<template>
    <div class="wrapper">
    <swiper :options="swiperOption" ref="mySwiper" >
    <!-- slides -->
    <swiper-slide v-for="item of imgitem" :key="item.id">
        <img :src="item.src"  class="swiper-img">
    </swiper-slide>
    
    
   <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  
  </div>    
</template>

<script>
export default {
  name: "HomeSwpier",
  data() {
    return {
      swiperOption: {
        pagination: ".swiper-pagination",
        loop: true
      },
      imgitem: [
        {
          id: "001",
          src:
            "http://img1.qunarzz.com/piao/fusion/1805/3b/ef86879aa50e3002.jpg_750x200_2a108508.jpg"
        },
        {
          id: "002",
          src:
            "http://img1.qunarzz.com/piao/fusion/1806/3c/5e0ea26abdf81302.jpg_750x200_1cba021d.jpg"
        }
      ],
    
      
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active {
    background: #fff;
}

.wrapper {
    overflow: hidden;
    width: 100%;
    height: 0;
    padding-bottom: 26.25%;
    background: #eee;

    .swiper-img {
        width: 100%;
    }
}
</style>
