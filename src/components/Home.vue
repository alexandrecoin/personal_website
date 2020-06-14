<template>
  <div class="container">
    <h1>{{ title }}</h1>
    <p class="intro">
      Have you been dreaming of a website or an application ? I know you have !
      And I would be very pleased to help you achieve that goal. If you ever
      feel that we could work together, do not hesitate to contact me through
      the "Contact" section above.
    </p>
    <div class="application">
      <img
        src="../assets/web_app.png"
        alt="web-app_picture"
        class="application_img"
      />
      <div class="application_description">
        <h3>Web applications</h3>
        <p>
          Since I've started coding, my main focus has primarily been web
          applications. I can help you design from sratch your project.
        </p>
      </div>
    </div>

    <div class="website">
      <div class="website_description">
        <h3>Websites</h3>
        <p>
          Web apps are not the only product I can do for you. If you are looking
          for a sleek website, whether it is for a landing page, e-commerce or
          for any kind of business, I can do it too.
        </p>
      </div>
      <img
        src="../assets/website.jpg"
        alt="website_picture"
        class="website_img"
      />
    </div>

    <div class="mobile_app">
      <img
        src="../assets/mobile_app.png"
        alt="web-app_picture"
        class="mobile_app_img"
      />
      <div class="mobile_app_description">
        <h3>Mobile applications</h3>
        <p>
          Thanks to technologies such as React Native, you no longer need to
          develop different codebases depending on your targeted device. One
          code base, all available platforms, it's as simple as that !
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      title: 'Get the product you dream of.',
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  height: 90%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.intro {
  max-width: 70%;
  text-justify: auto;
}

.application,
.website,
.mobile_app {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  max-width: 70%;
  margin-top: 6%;
  /* background-color: red; */
}

.application_img,
.website_img,
.mobile_app_img {
  max-width: 30%;
  border-radius: 1em;
  box-shadow: 5px 5px #ffffff;
}

.application_description,
.website_description,
.mobile_app_description {
  max-width: 50%;
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

@media (max-width: 640px) {
  .container {
    flex-direction: column;
  }

  .application,
  .website,
  .mobile_app {
    flex-direction: column;
    align-items: center;
  }

  .application_img,
  .website_img,
  .mobile_app_img {
    max-width: 80%;
    border-radius: 0.5em;
  }

  .application_description,
  .website_description,
  .mobile_app_description {
    max-width: 80%;
  }

  .website {
    flex-direction: column-reverse;
  }
}
</style>
