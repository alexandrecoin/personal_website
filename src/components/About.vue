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
      <p class="intro">{{ about.description.intro }}</p>

      <h3 class="techs_title">I am using on a daily basis :</h3>
      <div class="techs">
        <ul
          v-for="(techno, index) in technos"
          :key="index"
          class="technos_list"
        >
          <li class="techno">
            <p class="techno_name">{{ techno.name }}</p>
            <img :src="techno.path" v-bind:alt="techno.name" class="logo" />
          </li>
        </ul>
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
          path: require('../assets/technos/js_logo.png'),
        },
        {
          name: 'Vue.js',
          path: require('../assets/technos/vue_logo.png'),
        },
        {
          name: 'Node',
          path: require('../assets/technos/node_logo.png'),
        },
        {
          name: 'NestJS',
          path: require('../assets/technos/nestjs_logo.png'),
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  margin-top: 3%;
  height: 90%;
  max-width: 100vw;
}

.text-container {
  max-width: 40vw;
}

.intro {
  text-align: left;
  line-height: 2em;
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

.techs_title {
  margin-top: 10%;
}

.techs {
  display: flex;
  flex-direction: row;
  margin-right: 5vw;
}

.technos_list {
  margin-right: 1vw;
  max-width: 10vw;
  list-style-type: none;
}

/* .techno {
  flex-direction: column;
  align-content: center;
} */

.logo {
  max-height: 80px;
}

@media (max-width: 640px) {
  .container {
    flex-direction: column;
    align-items: center;
    margin-top: 12%;
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

  .techs {
    display: flex;
    flex-direction: column;
    margin-bottom: 2vh;
    margin-left: 20%;
  }

  .techno_name {
    display: none;
  }
}
</style>
