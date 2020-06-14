<template>
  <div class="container">
    <img
      src="../assets/profile_picture.png"
      alt="profilePicture"
      class="profile-pic1"
    />
    <img
      src="../assets/small_profile_picture.png"
      alt="smallProfilePicture"
      class="profile-pic2"
    />
    <div class="text-container">
      <h2>{{ about.title }}</h2>
      <p>{{ about.description.intro }}</p>
      <p>{{ about.description.main }}</p>
      <div class="buttons">
        <button value="french" @click="downloadResume($event)">
          Download (French)
        </button>
        <!-- <a
          :href="require('../assets/resume/coin_alexandre_resume_french.pdf')"
          download
          >Download (French)</a
        > -->
        <button value="english" @click="downloadResume">
          Download (English)
        </button>
      </div>
      <div class="techs">
        <h3>Techs I am using:</h3>
        <!-- <ul v-for="(techno, index) in technos" :key="index" class="technos_list">
          <li>
            <div >
              <h3>{{ techno.name }}</h3>
              <img :src="getPicture(techno.path)" v-bind:alt="techno.name" /> 
              <h3>JavaScript</h3>
              <img src="../assets/technos/js_logo.png" alt="js_logo" class="logo" />
            </div>
          </li>
        </ul> -->
      </div>
    </div>
  </div>
</template>
<script>
import about from '../data/data';
export default {
  name: 'About',
  data() {
    return {
      about,
      technos: [
        {
          name: 'JavaScript',
          path: 'js_logo',
        },
        {
          name: 'Vue.js',
          path: 'vue_logo',
        },
        {
          name: 'React',
          path: 'react_logo',
        },
        {
          name: 'Node',
          path: 'node_logo',
        },
        {
          name: 'NestJS',
          path: 'nestjs_logo',
        },
      ],
    };
  },
  methods: {
    downloadResume(e) {
      console.log(e.target.value)
    },
    // getPicture(path) {
    //   console.log('../assets/technos/' + path + '.png');
    //   return '../assets/technos/' + path + '.png';
    // },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin-top: 7%;
}

.text-container {
  max-width: 40vw;
}

.buttons {
  display: flex;
  flex-direction: row;
  justify-content: space-around;
}

.profile-pic1 {
  border-radius: 1em;
  margin-top: 3%;
}

.profile-pic2 {
  display: none;
}

.technos_list {
  display: flex;
  flex-direction: row;
}

.logo {
  max-height: 10%;
}

@media (max-width: 640px) {
  .container {
    flex-direction: column;
    align-items: center;
  }

  .buttons {
    display: flex;
    flex-direction: column;
    justify-content: space-around;
  }
  .profile-pic1 {
    display: none;
  }

  .profile-pic2 {
    display: block;
    border-radius: 50%;
    max-width: 30vw;
    margin-top: 20%;
  }

  .text-container {
    max-width: 90%;
  }
}
</style>
