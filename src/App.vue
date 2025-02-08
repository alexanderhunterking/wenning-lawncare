<template>
  <div id="app">
    <NavBar />
    <div class="container mt-5">
      <h1>Welcome to Wenning Lawncare & Landscaping</h1>
      <p>Your trusted partner for all your lawncare and landscaping needs.</p>
    </div>
    <Footer />
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
  }
}
</script>

<style>
body {
  font-family: Arial, sans-serif;
}
</style>