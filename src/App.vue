<template>

  <HeaderComponent />
  <main>
    <HomeView msg="Welcome to Your Vue.js App" />
  </main>
  <FooterComponent />
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HomeView from './views/Home.vue'
// import Acerca from './views/Acerca.vue'

export default {
  name: 'App',
  components: {
    HomeView,
    HeaderComponent, FooterComponent
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

  /* margin-top: 60px; */


}

.imagenpex {
  filter: drop-shadow(30px 10px 15px #0707077e) contrast(130%);
}



body {
  padding: 0%;
  margin: 0%;
  /* background: linear-gradient(225deg, #18011e 0%, #101d44 100%); */
}
</style>
