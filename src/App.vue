<template>
  <div id="app">
    <Navbar />
    <router-view></router-view>
    <Footer />
  </div>
</template>

<script>
import Navbar from './layout/Navbar.vue';
import Footer from './layout/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Footer,
  },
};
</script>

<style>
body {
  background-color: #f1f1f1;
  /* background: linear-gradient(150deg, #fdcd3b 10%, #ffed4b 50%); */
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
</style>
