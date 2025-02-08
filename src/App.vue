<template>
  <!--
  <div :class="theme">
    <NavBar :theme="theme" />
    <div class="container mt-5">
      <h1>Welcome to Wenning Lawncare & Landscaping</h1>
      <p>Your trusted partner for all your lawncare and landscaping needs.</p>
    </div>
    <Footer @toggle-theme="toggleTheme" :theme="theme" />
  </div>
  -->
  <div class="d-flex flex-column justify-content-center align-items-center vh-100 text-light bg-dark">
    <i class="bi bi-exclamation-triangle-fill" style="font-size: 3rem;"></i>
    <h1>The new Wenning lawncare and landscape website is currently under development</h1>
    <p class="text-light">stay tuned ;)</p>
  </div>
</template>

<script>
/*
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
*/
</script>

<style>
body {
  font-family: Arial, sans-serif;
}

body.light-mode {
  background-color: white;
  color: black;
}

body.dark-mode {
  background-color: #121212;
  color: white;
}

.vh-100 {
  height: 100vh;
}
</style>