<template>
    <footer :class="['footer', theme, 'text-center', 'text-lg-start', 'theme-transition']">
      <div class="text-center p-3">
        © 2025 Lawncare & Landscaping:
        <a :class="theme === 'dark-mode' ? 'text-light' : 'text-dark'" href="https://example.com/">example.com</a>
        <button @click="toggleTheme" class="btn btn-secondary ms-3">Toggle Theme</button>
      </div>
    </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
    theme: {
      type: String,
      default: 'light-mode'
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
.footer {
  position: relative;
  left: 0;
  bottom: 0;
  width: 100%;
}

.theme-transition {
  transition: background-color 0.5s, color 0.5s;
}
</style>