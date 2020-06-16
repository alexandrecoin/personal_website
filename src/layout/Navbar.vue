<template>
  <div class="container">
    <ul id="links">
      <router-link class="link" to="/">Home</router-link>
      <!-- <router-link class="link" to="/work">Work</router-link> -->
      <router-link class="link" to="/about">About</router-link>
      <li class="twitter">
        <a href="https://www.twitter.com/lxndrcn" target="_blank" class="link"
          ><i class="fa fa-link" aria-hidden="true"></i> twitter</a
        >
      </li>
      <li class="github">
        <a
          href="https://www.github.com/alexandrecoin"
          target="_blank"
          class="link"
        > <i class="fa fa-link" aria-hidden="true"></i> github</a
        >
      </li>
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
  z-index: 1;
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  height: 7vh;
  position: fixed;
  background-color: #f1f1f1;
  top: 0;
  left: 0;
  right: 0;
}

h1 {
  font-size: 1em;
}

#links {
  list-style-type: none;
  margin-right: 4em;
  display: flex;
  flex-direction: row;
}

#links:hover {
  cursor: pointer;
}

.link {
  margin-right: 1em;
  text-decoration: none;
}

.link,
.link:visited {
  color: #2c3e50;
}

.router-link-exact-active {
  font-weight: bold;
}

@media (max-width: 640px) {
  .container {
    height: 15%;
  }

  #links {
    flex-direction: column;
    margin-right: 0.3em;
    align-items: flex-end;
  }
}
</style>
