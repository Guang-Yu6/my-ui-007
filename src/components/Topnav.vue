<template>
  <div class="topnav">
    <div class="logo" @click="toggleMenu">Logo</div>
    <ul class="menu">
      <li>菜单1</li>
      <li>菜单2</li>
    </ul>
  </div>
</template>

<script lang='ts'>
import {inject,Ref} from "vue";

export default {
  name: "Topnav",
  setup(){
    const menuVisible =  inject<Ref<boolean>>('xxx123')  // get
    console.log('Topnav +' + menuVisible.value)
    const toggleMenu = () =>{
      menuVisible.value = !menuVisible.value  // 取反赋值， x = x + 1
    }
    return {toggleMenu}
  }
}
</script>

<style lang='scss' scoped>
.topnav {
  background: pink;
  display: flex;
  padding: 16px;
  position: relative;
  z-index: 10;
  > .logo {
    max-width: 6em;
    margin-right: auto;
  }
  > .menu {
    display: flex;
    white-space: nowrap;
    flex-wrap: nowrap;
    > li {
      margin: 0 1em;
    }
  }
}
</style>