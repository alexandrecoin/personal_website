<template>
  <footer class="footer">
    <ul>
      <li class="twitter">
        <a href="https://www.twitter.com/lxndrcn" target="_blank"
          ><i class="fab fa-twitter "></i
        ></a>
      </li>
      <li class="github">
        <a href="https://www.github.com/alexandrecoin" target="_blank">
          <i class="fab fa-github "></i
        ></a>
      </li>
    </ul>
  </footer>
</template>

<style scoped>
ul {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  list-style-type: none;
}

a,
a:visited {
  color: #2c3e50;
}

.github {
  margin-right: 5%;
  font-size: 2em;
}

.twitter {
  margin-right: 8%;
  font-size: 2em;
}
</style>
