<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <transition name="fade" mode="out-in">
      <router-view/>
    </transition>
    
    
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
// transition动画
.fade-enter-active,.fade-leave-active{
    transition: all 0.2s;
  }
  .fade-enter,.fade-leave-to{
    position:relative;
    top: 100px;
   opacity: 0;
  }
  .fade-enter-to,.fade-leave{
    position:relative;
    top: 0;
   opacity: 1;
  }
 
 
</style>
