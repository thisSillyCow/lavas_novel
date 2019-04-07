<template>
  <div class="page-index">
    <router-view></router-view>
    <tabs></tabs>
  </div>
</template>

<script>
import tabs from "../components/tabs";
export default {
  name: "index",
  components: {
    tabs
  }
};
</script>

<style lang="less" scoped>
.page-index {
  display: flex;
  overflow: hidden;
}
</style>
