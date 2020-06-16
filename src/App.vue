<template>
  <div id="app">
    <Navbar
      :style="{ background: scrollPosition < 50 ? '#efefef' : 'white' }"
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
      toggleSwitch: document.querySelector(
        '.theme-switch input[type="checkbox"]',
      ),
      currentTheme: localStorage.getItem('theme')
        ? localStorage.getItem('theme')
        : null,
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
    checkTheme() {
      console.log(this.currentTheme);
      if (this.currentTheme) {
        document.documentElement.setAttribute('data-theme', this.currentTheme);

        if (this.currentTheme === 'dark') {
          console.log('oook');
          this.toggleSwitch.checked = true;
        }
      }
    },
  },
  mounted() {
    window.addEventListener('scroll', this.updateScroll);
    console.log(document.querySelector('.theme-switch input[type="checkbox"]').value);
    this.checkTheme();
  },
};
</script>

<style>
:root {
  --primary-color: #302ae6;
  --secondary-color: #536390;
  --font-color: #2c3e50;
  --bg-color: #f1f1f1;
  --heading-color: #292922;
  --box-shadow-left-color: #b7b7b7;
  --box-shadow-right-color: #ffffff;
  --box-shadow-left: 7px 7px 14px;
  --box-shadow-right: -7px -7px 14px;
}

[data-theme='dark'] {
  --card-color: #403f3d;
  --primary-color: #9a97f3;
  --secondary-color: #818cab;
  --font-color: #e1e1dd;
  --bg-color: #272727;
  --heading-color: #818cab;
  --box-shadow-left-color: #171717;
  --box-shadow-right-color: #373737;
  --box-shadow-left: 7px 7px 14px;
  --box-shadow-right: -7px -7px 14px;
}

body {
  background-color: var(--bg-color);
  color: var(--font-color);
}

#app {
  font-family: 'Arimo', sans-serif;

  /* font-family: Avenir, Helvetica, Arial, sans-serif; */
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
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
