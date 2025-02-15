<template>
  <div :class="theme" class="theme-transition">
    <NavBar :theme="theme" @toggle-theme="toggleTheme" />
    <div class="banner">
      <img :src="bannerImage" alt="Banner" class="banner-image">
    </div>
    <div class="container mt-5">
      <div class="row">
        <div class="col-12 text-center">
          <h2>About Us</h2>
        </div>
      </div>
      <div class="container about-section">
        <div class="row justify-content-center align-items-center">
          <div class="col-md-4 order-2 order-md-1 text-center about-text">
            <div :class="['text-box', theme]">
              <p>Jordan Wenning and his company have been offering exceptional service to the Pendleton community since 2017. He started out of his parent's garage with just a push-mower. He has since grown his hobby into a full blown professional operation with top of the line equipment and a dedicated property.</p>
            </div>
          </div>
          <div class="col-md-2 order-3 order-md-2"></div>
          <div class="col-md-4 text-center order-1 order-md-3">
            <img :src="aboutImage" alt="Jordan Wenning" class="about-image">
          </div>
        </div>
      </div>
    </div>
    <Footer @toggle-theme="toggleTheme" :theme="theme" />
  </div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'
import bannerImage from './assets/JordanWenning-2930_Original.JPG'
import aboutImage from './assets/JordanWenning-2753_Original.JPG'

export default {
  name: 'App',
  components: {
    NavBar,
    Footer
  },
  data() {
    return {
      theme: 'dark-mode',
      bannerImage,
      aboutImage
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

.about-section {
  display: flex;
  align-items: center;
}

.about-text {
  display: flex;
  align-items: center;
  height: 100%;
}

.text-box {
  padding: 20px;
  border-radius: 10px;
  transition: background-color 0.5s, color 0.5s;
}

.text-box.dark-mode {
  background-color: #2c2c2c; /* Slightly lighter gray than the background */
}

.text-box.light-mode {
  background-color: #f0f0f0; /* Very light grey */
}

.about-image {
  width: 100%;
  height: auto;
  border-radius: 50%;
}

@media (max-width: 768px) {
  .about-image {
    width: 70%;
  }
}
</style>