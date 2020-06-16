<template>
  <div class="theme-switch-wrapper">
    <em class="light-mode">&#9728;</em>
    <label class="theme-switch" for="checkbox">
      <input type="checkbox" id="checkbox" @click="switchTheme($event)" />
      <div class="slider round"></div>
    </label>
    <em>&#9790;</em>
  </div>
</template>

<script>
export default {
  methods: {
    switchTheme(e) {
      if (e.target.checked) {
        document.documentElement.setAttribute('data-theme', 'dark');
        localStorage.setItem('theme', 'dark');
      } else {
        document.documentElement.setAttribute('data-theme', 'light');
        localStorage.setItem('theme', 'light');
      }
    },
  },
};
</script>

<style scoped>
.theme-switch-wrapper {
  display: flex;
  align-items: center;
}
em {
  margin-left: 10px;
  font-size: 1rem;
}

.theme-switch {
  display: inline-block;
  height: 34px;
  position: relative;
  width: 60px;
}

.light-mode {
  margin-right: 0.8em;
}

.theme-switch input {
  display: none;
}

.slider {
  background-color: #ccc;
  bottom: 0;
  cursor: pointer;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transition: 0.4s;
}

.slider:before {
  background-color: #fff;
  bottom: 4px;
  content: '';
  height: 26px;
  left: 4px;
  position: absolute;
  transition: 0.4s;
  width: 26px;
}

input:checked + .slider {
  background-color: #66bb6a;
}

input:checked + .slider:before {
  transform: translateX(26px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}

#card {
  background-color: var(--card-color);
  box-shadow: var(--box-shadow-left) var(--box-shadow-left-color),
    var(--box-shadow-right) var(--box-shadow-right-color);
}
</style>
