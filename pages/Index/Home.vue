<template>
  <div class="page-index">
    <Swiper></Swiper>
    <!-- <div>1111111111111111111111111111111</div> -->
  </div>
</template>

<script>
import Swiper from "../../components/swiper";
export default {
  name: "index",
  metaInfo: {
    titleTemplate: "首页"
  },
  components: {
    Swiper
  }
};
</script>

<style lang="less" scoped>
.page-index {
  flex: 1;
  justify-content: center;
  //   align-items: center;
}
</style>