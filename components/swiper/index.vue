
<template>
  <swiper :options="swiperOption" class="page-index">
    <swiper-slide
      v-for="(slide, index) in swiperSlides"
      :key="index"
      class="swiper-slide-index"
    >
      I'm Slide {{ slide }}
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "index",
  metaInfo: {
    titleTemplate: "首页"
  },
  data() {
    return {
      swiperOption: {
        pagination: {
          el: ".swiper-pagination"
        },
        autoplay: {
          stopOnLastSlide: true,
          delay: 4000
        }
      },
      swiperSlides: [1, 2, 3, 4, 5]
    };
  },
  mounted() {
    // setInterval(() => {
    //   console.log("simulate async data");
    //   if (this.swiperSlides.length < 10) {
    //     this.swiperSlides.push(this.swiperSlides.length + 1);
    //   }
    // }, 3000);
  },
  components: {
    swiper,
    swiperSlide
  }
};
</script>

<style lang="less" scoped>
.page-index {
  width: 100%;
  height: 200px;
}
.swiper-slide-index {
  text-align: center;
  line-height: 200px;
  width: 100%;
  height: 200px;
}
</style>
