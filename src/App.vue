<template>
  <div :class="theme" class="theme-transition">
    <NavBar :theme="theme" @toggle-theme="toggleTheme" />
    <div class="banner">
      <img src="./assets/JordanWenning-2930_Original.JPG" alt="Banner" class="banner-image">
    </div>
    <div class="container mt-5">
      <h1>Welcome to Wenning Lawncare & Landscaping</h1>
      <p>Your trusted partner for all your lawncare and landscaping needs.</p>
    </div>
    <Footer @toggle-theme="toggleTheme" :theme="theme" />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    NavBar,
    Footer
  },
  data() {
    return {
      theme: 'dark-mode'
    }
  },
  methods: {
    toggleTheme() {
      this.theme = this.theme === 'dark-mode' ? 'light-mode' : 'dark-mode';
    }
  },
  watch: {
    theme(newTheme, oldTheme) {
      document.body.classList.remove(oldTheme);
      document.body.classList.add(newTheme);
    }
  },
  mounted() {
    document.body.classList.add(this.theme);
  }
}
</script>

<style>
body.light-mode {
  background-color: white;
  color: black;
  transition: background-color 0.5s, color 0.5s;
}

body.dark-mode {
  background-color: #121212;
  color: white;
  transition: background-color 0.5s, color 0.5s;
}

.theme-transition {
  transition: background-color 0.5s, color 0.5s;
}

.banner {
  width: 100%;
  height: auto;
  margin-top: -56px; /* Adjust based on the height of the navbar */
}

.banner-image {
  width: 100%;
  height: auto;
}
</style>