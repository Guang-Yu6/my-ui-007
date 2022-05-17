<template>
  <div>
    <topnav/>
    <div class="top-nav">
      <div class="logo"></div>
      <div class="menu"></div>
    </div>

    <div class="content">
      <aside>边栏</aside>
      <main>主要内容</main>
    </div>
  </div>
</template>

<script>
import Topnav from "../components/Topnav.vue";
export default {
  components: {Topnav}
}
</script>

<style lang="scss" scoped>
aside {
  background: lightblue;
  width: 150px;
  padding: 16px;
  position: fixed;
  top: 0;
  left: 0;
  padding-top: 80px;
  > h2 {
    margin-bottom: 4px;
  }
  > ol {
    > li {
      padding: 4px 0;
    }
  }
}
</style>

