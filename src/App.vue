<template>
  <div id="app">
    <Navbar
      :style="{ background: scrollPosition < 50 ? '#f1f1f1' : 'white' }"
    />
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
  data() {
    return {
      scrollPosition: null,
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
  },
};
</script>

<style>
body {
  background-color: #f1f1f1;
  /* background: linear-gradient(150deg, #fdcd3b 10%, #ffed4b 50%); */
}

#app {
  font-family: 'Arimo', sans-serif;
  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

h1 {
  font-size: 4em;
}

h2 {
  font-size: 2em;
}

h3 {
  font-size: 1.5em;
}
</style>
