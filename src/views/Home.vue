<template>
  <div class="home">
    <button @click="isShow = !isShow">show/hide</button>
    <transition name="fade">
      <HelloWorld v-show="isShow" msg="Welcome to Your Vue.js App"/>
    </transition>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  },
  data(){
    return {
      isShow:true
    }
  }
}
</script>

<style lang="scss" scoped>
  

  
</style>
