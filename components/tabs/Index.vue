<template>
  <div class="page-index">
    <div class="tabs" v-on:click="homeActive('home')">
      <div>
        <img v-if="isActiveHome" src="../../image/bookCityOutline.png" />
        <img v-else src="../../image/bookCity.png" />
      </div>
      <span v-bind:class="{ active: isActiveHome }">首页</span>
    </div>
    <div class="tabs" v-on:click="homeActive('class')">
      <div>
        <img v-if="isActiveClass" src="../../image/statsOutline.png" />
        <img v-else src="../../image/unstats.png" />
      </div>
      <span v-bind:class="{ active: isActiveClass }">分类</span>
    </div>
    <div class="tabs" v-on:click="homeActive('Bookshelf')">
      <div>
        <img v-if="isActiveBookshelf" src="../../image/bookshelfOutlie.png" />
        <img v-else src="../../image/bookshelf.png" />
      </div>
      <span v-bind:class="{ active: isActiveBookshelf }">书架</span>
    </div>
    <div class="tabs" v-on:click="homeActive('min')">
      <div>
        <img v-if="isActiveMin" src="../../image/personOutline.png" />
        <img v-else src="../../image/personNor.png" />
      </div>
      <span v-bind:class="{ active: isActiveMin }">我的</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActiveHome: true,
      isActiveClass: false,
      isActiveBookshelf: false,
      isActiveMin: false
    };
  },
  methods: {
    homeActive(tabsType) {
      this.isActiveHome = false;
      this.isActiveClass = false;
      this.isActiveBookshelf = false;
      this.isActiveMin = false;
      if (tabsType == "home") {
        this.isActiveHome = true;
        this.$router.push({ path: "/" });
      } else if (tabsType == "class") {
        this.isActiveClass = true;
        this.$router.push({ path: "classification" });
      } else if (tabsType == "Bookshelf") {
        this.isActiveBookshelf = true;
        this.$router.push({ path: "bookshelf" });
      } else if (tabsType == "min") {
        this.isActiveMin = true;
        this.$router.push({ path: "mine" });
      }
    }
  },
  created() {
    this.homeActive("home");
  }
};
</script>

<style lang="less" scoped>
@tabsh : 3.5rem;
@import "../../assets/color/Index.less";
.page-index {
  display: flex;
  position: absolute;
  bottom: 0;
  right: 0;
  left: 0;
  justify-content: space-between;
  align-items: center;
  height: @tabsh;
  border-top-color: #e9e9e9;
  border-top-width: 0.5px;
  border-top-style: solid;
  background: #fff;
}
.tabs {
  flex: 1;
  font-size: 12px;
  font-weight: 400;
  color: @textTabInitColor;
  flex-direction: column;
  align-items: center;
}
.active {
  color: @themeColor;
}
</style>