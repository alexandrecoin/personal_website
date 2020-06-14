<template>
  <div class="main">
    <h1>{{ title }}</h1>
    <p>Welcome to my personal website !</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      title: 'Another JS developer',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.main {
  height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

h1 {
  display: block;
}
</style>
