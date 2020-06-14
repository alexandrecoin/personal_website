<template>
  <div class="container">
    <router-link class="home" to="/"><h1>Home</h1></router-link>
    <ul id="links">
      <router-link class="link" to="/">Work</router-link>
      <router-link class="link" to="/about">About</router-link>
      <router-link class="link" to="/">Articles</router-link>
      <router-link class="link" to="/contact">Contact</router-link>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  height: 5vh;
}

h1 {
  font-size: 1em;
}

.home {
  margin-left: 2em;
}

#links {
  list-style-type: none;
  margin-right: 3em;
  display: flex;
  flex-direction: row;
}

#links:hover {
  cursor: pointer;
}

.link,
.home {
  margin-right: 1em;
  text-decoration: none;
}

.link,
.home,
.link:visited,
.home:visited {
  color: #2c3e50;
}
</style>
