<template>
    <nav :class="['navbar', 'navbar-expand-lg', theme === 'dark-mode' ? 'navbar-dark' : 'navbar-light', isScrolled ? (theme === 'dark-mode' ? 'bg-dark-green' : 'bg-light-green') : 'bg-transparent', 'theme-transition', 'fixed-top']">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"><img :src="logoSrc" alt="Wenning Lawncare & Landscaping" class="navbar-logo"></a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#about-section">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#reviews-section">Reviews</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Services</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#gallery-section">Gallery</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Contact</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
</template>

<script>
import darkLogo from '../assets/darkmodelogo.png';
import lightLogo from '../assets/lightmodelogo.png';

export default {
  name: 'NavBar',
  props: {
    theme: {
      type: String,
      default: 'dark-mode'
    }
  },
  data() {
    return {
      darkLogo,
      lightLogo,
      isScrolled: false
    };
  },
  computed: {
    logoSrc() {
      return this.theme === 'dark-mode' ? this.darkLogo : this.lightLogo;
    }
  },
  methods: {
    toggleTheme() {
      this.$emit('toggle-theme');
    },
    handleScroll() {
      this.isScrolled = window.scrollY > 50;
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  }
}
</script>

<style scoped>
.bg-light-green {
  background-color: #d4edda;
}

.bg-dark-green {
  background-color: #155724;
}

.bg-transparent {
  background-color: transparent;
}

.navbar-logo {
  height: 40px;
  width: auto;
}

.theme-transition {
  transition: background-color 0.5s, color 0.5s;
}

.fixed-top {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1030;
}
</style>