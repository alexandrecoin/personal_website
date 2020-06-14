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
    };
  },
  methods: {
    downloadResume() {},
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
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
    margin-top: 10%;
  }

  .text-container {
    max-width: 90%;
  }
}
</style>
