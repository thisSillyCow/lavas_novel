<template>
  <div class="page-index">分类</div>
</template>

<script>
export default {
  name: "classification",
  metaInfo: {
    title: "分类",
    titleTemplate: "%s - Lavas",
    meta: [
      { name: "keywords", content: "lavas PWA" },
      {
        name: "description",
        content:
          "基于 Vue 的 PWA 解决方案，帮助开发者快速搭建 PWA 应用，解决接入 PWA 的各种问题"
      }
    ]
  }
};
</script>

<style lang="less" scoped>
.page-index {
  flex: 1;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
</style>