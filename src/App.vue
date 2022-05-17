<template>
  <div>
    <router-view/>
  </div>
</template>

<script>
import {ref,provide} from 'vue'

export default {
  name: 'App',
  components: {

  },
  setup(){
    const menuVisible = ref(false)
    provide('xxx123',menuVisible)  // set  ,标记为所有的后代组件都可以使用它，暗号就是''里的字符串类型
  }
}
</script>
