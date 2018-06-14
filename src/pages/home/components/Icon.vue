<template>
    <div class="icons">

        <swiper :options="swiperOption" ref="mySwiper" >
            <swiper-slide v-for="page of pages" >
            <div class="icon-item" v-for="item of page">
                <div class="icon-img">
                <img :src="item.imgSrc" alt="" width="100%" >
                </div>
                <p class="icon-desc">{{item.desc}}</p>
            </div>
           
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
  name: "HomeIcon",
  data() {
    return {
      imgitem: [
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png",
          desc: "景点门票"
        },
        
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png",
          desc: "必游榜单"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png",
          desc: "动植物园"
        },

        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png",
          desc: "公园"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/bd/9f7b9b2b60c1502.png",
          desc: "游船游艇"
        },
        {
          id: "6",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png",
          desc: "路清赏花"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png",
          desc: "历史古迹"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png",
          desc: "一日游"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png",
          desc: "玩转长隆"
        },
        {
          id: "1",
          imgSrc:
            "http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png",
          desc: "全部玩乐"
        }
      ]
    };
  },
  computed: {
    data() {
      return {
        swiperOption: {
          loop: true,
          pagination: ".swiper-pagination"
        }
      };
    },
    pages() {
      const pages = [];
      this.imgitem.forEach((item, index) => {
        const page = Math.floor(index / 8);
        if (!pages[page]) {
          pages[page] = [];
        }
        pages[page].push(item);
      });
      return pages;
    }
  }
};
</script>

<style lang="stylus" scoped>
.icons {
    overflow: hidden;
    height: 0;
    padding-bottom: 50%;
    background-color: #eee;

    .icon-item {
        position: relative;
        overflow: hidden;
        float: left;
        width: 25%;
        height: 0;
        padding-bottom: 25%;

        .icon-img {
            width: 100%;
            box-sizing: border-box;
            padding: 0.1rem;
        }

        .icon-desc {
            position: absolute;
            left: 0;
            right: 0;
            bottom: -0.2rem;
            height: 0.44rem;
            line-height: 0.44rem;
            text-align: center;
            color: $darkTextColor;
        }
    }
}
</style>
