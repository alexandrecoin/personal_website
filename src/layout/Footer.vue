<template>
  <footer class="footer">
    <p class="contact">
      <span class="text">Any request or just want to say hi ? </span>Let's get in touch
      :
      <span
        ><a href="mailto:alexandre.pc.coin@gmail.com"
          ><i class="fa fa-envelope" aria-hidden="true"></i></a
      ></span>
    </p>
  </footer>
</template>

<style scoped>
footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  height: 3%;
}

a,
a:visited {
  color: #2c3e50;
}

.contact {
  margin-right: 5%;
}

@media (max-width: 640px) {
  .text {
    display: none;
  }

  .fa-envelope {
    font-size: 1em;
  }
}
</style>
