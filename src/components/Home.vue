<template>
  <div class="container">
    <h1 class="full-title">{{ fullTitle }}</h1>
    <h1 class="mobile-title">{{ mobileTitle }}</h1>
    <p class="intro">
      {{ intro }}
    </p>
    <h2>What I do</h2>
    <div class="application">
      <img
        src="../assets/web_app.png"
        alt="web-app_picture"
        class="application_img"
      />
      <div class="application_description">
        <h3>Web applications</h3>
        <p class="text">
          Since I've started coding, my main focus has primarily been web
          applications. With experience in Fintech and Edtech companies, I can
          help you design your project from sratch.
        </p>
      </div>
    </div>

    <div class="website">
      <div class="website_description">
        <h3>Websites</h3>
        <p class="text">
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
        <p class="text">
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
      fullTitle: 'Hello ! How can I help you ?',
      mobileTitle: 'Hello !',
      intro: `Hello there ! My name is Alexandre, and I'm a full-stack developer. I am currently looking for a new position. 
      If you're visiting this website, you may have you been dreaming of a website or an application, no ? I know you have!
      I would be very pleased to help you build it. If you ever happen to like what I've done or
      feel that we could work together, do not hesitate to contact me.`,
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
  margin-top: 5%;
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
  max-width: 80%;
  margin-top: 1%;
  padding: 3% 0%;
}

.application_img,
.website_img,
.mobile_app_img {
  max-width: 30%;
  border-radius: 1em;
  box-shadow: 20px 20px 42px #d9d9d9, -20px -20px 42px #ffffff;
}

.application_description,
.website_description,
.mobile_app_description {
  max-width: 50%;
}

.intro,
.text {
  line-height: 2em;
  text-align: left;
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

@media (min-width: 640px) {
  .application_img,
  .website_img,
  .mobile_app_img {
    transition: transform 1s ease-in-out;
  }

  .mobile-title {
    display: none;
  }

  .application_img:hover,
  .website_img:hover,
  .mobile_app_img:hover {
    transform: scale(1.1);
  }
}

@media (max-width: 640px) {
  .container {
    flex-direction: column;
    margin-top: 25%;
  }

  .full-title {
    display: none;
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
