<template>
    <nav :class="['navbar', 'navbar-expand-lg', theme === 'dark-mode' ? 'navbar-dark bg-dark-green' : 'navbar-light bg-light-green']">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Wenning Lawncare & Landscaping</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
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
  export default {
    name: 'NavBar',
    props: {
      theme: {
        type: String,
        default: 'light-mode'
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
  </style>