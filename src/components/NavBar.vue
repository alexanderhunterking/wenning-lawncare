<template>
    <nav :class="['navbar', 'navbar-expand-lg', theme === 'dark-mode' ? 'navbar-dark bg-dark-green' : 'navbar-light bg-light-green']">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"><img :src="logoSrc" alt="Wenning Lawncare & Landscaping" class="navbar-logo"></a>
        <button class="navbar-toggler" type="button" @click="toggleTheme" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav ms-auto">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">About</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Reviews</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Services</a>
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
      lightLogo
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
    }
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
.navbar-logo {
  height: 40px;
  width: auto;
}
</style>