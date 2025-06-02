<template>
  <div :class="theme" class="theme-transition">
    <NavBar :theme="theme" @toggle-theme="toggleTheme" />
    <div class="banner">
      <img :src="bannerImage" alt="Banner" class="banner-image">
    </div>
    <div class="container mt-5 mb-5">
      <!-- about section -->
  <div class="row mb-3">
    <section class="py-5">
	    <div class="container about-section">
		      <div class="row align-items-center gx-4">
			<div class="col-md-5">
				<div class="ms-md-2 ms-lg-5"><img class="img-fluid rounded-3" :src="aboutImage"></div>
			</div>
			<div class="col-md-6 offset-md-1" :class="[theme]">
				<div class="ms-md-2 ms-lg-5">
					<h2 class="display-5 fw-bold">About Us</h2>
					<p class="lead">We have been offering exceptional service to the Pendleton community since 2017. Jordan Wenning started out of his parent's garage with just a push-mower. He has since grown his hobby into a full blown professional operation with top of the line equipment and a dedicated property.</p>
					<p class="lead mb-0">It doesn't matter if you just need weekly mowing, or you want to completely transform your property, we can gaurantee top notch quality. Get a quote for your project today!</p>
				</div>
			</div>
		</div>
	</div>
</section>
    </div>
    </div>
    <Footer @toggle-theme="toggleTheme" :theme="theme"/>
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
  height: 400px; /* Set a fixed height for the banner */
  margin-top: -56px; /* Adjust based on the height of the navbar */
  overflow: hidden;
}

.banner-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
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
  width: 70%;
  height: auto;
  border-radius: 50%;
}

@media (max-width: 768px) {
  .about-image {
    width: 50%;
  }
}
</style>