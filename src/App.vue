<template>
  <img class="imagenpex" alt="Vue logo" src="./assets/pez1.png">
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <HelloWorld msg="Welcome to Your Vue.js App" />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1b61a8;
  margin-top: 60px;


}
.imagenpex {
    filter: drop-shadow(30px 10px 15px #0707077e) contrast(130%);
}



body{

background: linear-gradient(225deg, #18011e 0%, #101d44 100%);
}
</style>
