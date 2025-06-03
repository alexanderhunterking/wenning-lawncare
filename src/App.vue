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
          <div class="container about-section" id="about-section" :class="[theme]">
            <div class="row align-items-center gx-4">
              <div class="col-md-5">
                <div class="ms-md-2 ms-lg-5 mb-4 mt-4">
                  <img class="img-fluid rounded-3" :src="aboutImage">
                </div>
              </div>
              <div class="col-md-6 offset-md-1">
                <div class="ms-md-2 ms-lg-5">
                  <h2 class="display-5 fw-bold">About Us</h2>
                  <p class="lead">We have been offering exceptional service to the Pendleton community since 2017. Jordan Wenning started out of his parent's garage with just a push-mower. He has since grown his hobby into a full blown professional operation with top of the line equipment and a dedicated property.</p>
                  <p class="lead mb-0">It doesn't matter if you just need weekly mowing, or you want to completely transform your property, we can guarantee top-notch quality. Get a quote for your project today!</p>
                </div>
              </div>
            </div>
          </div>
        </section>
      </div>
    </div>
    <!-- reviews section -->
    <div class="row mb-3">
      <section class="py-5">
        <div class="container" id="reviews-section">
          <div class="row justify-content-center text-center mb-2 mb-lg-4">
            <div class="col-12 col-lg-8 col-xxl-7 text-center mx-auto">
              <h2 class="display-5 fw-bold">Our Reviews</h2>
              <p class="lead">See what our clients are saying about our services!</p>
            </div>
          </div>
          <div class="row g-5 py-4 justify-content-center">
            <div class="col-lg-8">
              <div class="d-flex align-items-start mb-4">
                <img alt="" class="img-fluid rounded-circle me-3 review-image" height="96" src="https://freefrontend.dev/assets/square-small.png" width="96">
                <div :class="[theme === 'dark-mode' ? 'bg-dark' : 'bg-light']" class="p-3 p-md-4">
                  <div class="text-primary mb-1">
                    <svg class="bi bi-quote" fill="currentColor" height="32" viewbox="0 0 16 16" width="32" xmlns="http://www.w3.org/2000/svg">
                      <path d="M12 12a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1h-1.388c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 9 7.558V11a1 1 0 0 0 1 1h2Zm-6 0a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1H4.612c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 3 7.558V11a1 1 0 0 0 1 1h2Z"></path>
                    </svg>
                  </div>
                  <p class="lead">We've used Jordan & his team to maintain our lawn for the past year. Our project started with a detailed consultation to discuss the scope of work & design inspiration. From there, Jordan gave us a timeline/pricing estimates & we got scheduled. Communication was excellent throughout the process & the whole team was punctual & polite! We had a fairly large project so it was impressive that the team got it done in just 2 days. Absolutely thrilled with our "new yard"!</p>
                  <div class="text-end pt-2">
                    <h5 class="fw-bold">Victoria Spell</h5>
                  </div>
                </div>
              </div>
              <div class="d-flex align-items-start mb-4">
                <img alt="" class="img-fluid rounded-circle me-3 review-image" height="96" src="https://freefrontend.dev/assets/square-small.png" width="96">
                <div :class="[theme === 'dark-mode' ? 'bg-dark' : 'bg-light']" class="p-3 p-md-4">
                  <div class="text-primary mb-1">
                    <svg class="bi bi-quote" fill="currentColor" height="32" viewbox="0 0 16 16" width="32" xmlns="http://www.w3.org/2000/svg">
                      <path d="M12 12a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1h-1.388c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 9 7.558V11a1 1 0 0 0 1 1h2Zm-6 0a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1H4.612c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 3 7.558V11a1 1 0 0 0 1 1h2Z"></path>
                    </svg>
                  </div>
                  <p class="lead">Jordan and his team transformed our daughter’s home in only 2 days. They were great to work with, punctual and created a wonderful landscape. The work they did transformed the curb appeal of the house.</p>
                  <div class="text-end pt-2">
                    <h5 class="fw-bold">Lisa Sloan</h5>
                  </div>
                </div>
              </div>
              <div class="d-flex align-items-start mb-4">
                <img alt="" class="img-fluid rounded-circle me-3 review-image" height="96" src="https://freefrontend.dev/assets/square-small.png" width="96">
                <div :class="[theme === 'dark-mode' ? 'bg-dark' : 'bg-light']" class="p-3 p-md-4">
                  <div class="text-primary mb-1">
                    <svg class="bi bi-quote" fill="currentColor" height="32" viewbox="0 0 16 16" width="32" xmlns="http://www.w3.org/2000/svg">
                      <path d="M12 12a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1h-1.388c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 9 7.558V11a1 1 0 0 0 1 1h2Zm-6 0a1 1 0 0 0 1-1V8.558a1 1 0 0 0-1-1H4.612c0-.351.021-.703.062-1.054.062-.372.166-.703.31-.992.145-.29.331-.517.559-.683.227-.186.516-.279.868-.279V3c-.579 0-1.085.124-1.52.372a3.322 3.322 0 0 0-1.085.992 4.92 4.92 0 0 0-.62 1.458A7.712 7.712 0 0 0 3 7.558V11a1 1 0 0 0 1 1h2Z"></path>
                    </svg>
                  </div>
                  <p class="lead">My lawnmower broke and needed grass cut asap and he was there quickly. He did beautiful work in a very good time plus my lawn had amazing stripes. Very reasonable priced and amazing work. Would definitely recommend.</p>
                  <div class="text-end pt-2">
                    <h5 class="fw-bold">Jeff Jarvis</h5>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
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
  background-color: #1c1c1e;
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

.about-image {
  width: 70%;
  height: auto;
  border-radius: 50%;
}

.review-image {
  width: 96px;
  height: 96px;
}

@media (max-width: 768px) {
  .about-image {
    width: 50%;
  }

  .review-image {
    width: 64px;
    height: 64px;
  }
}
</style>