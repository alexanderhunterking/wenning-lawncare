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
              <div class="col-5 justify-content-center">
                <div class="ms-md-2 ms-lg-5 mb-4 mt-4">
                  <img class="img-fluid rounded-3 " :src="aboutImage">
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
    <!-- services section -->
     <div class="row mb-3">
      <section class="py-5" id="services-section">
	<div class="container">
		<div class="row justify-content-center text-center mb-3 mb-md-5">
			<div class="col-lg-8 col-xxl-7">
				<h2 class="display-5 fw-bold mb-3">Our Services</h2>
				<p class="lead">We specialize in professional lawncare and landscaping services that enhance the beauty and functionality of your outdoor spaces. From spring planting to winter snow removal, we provide tailored solutions for every season!</p>
			</div>
		</div>
		<div class="row row-cols-1 row-cols-md-3 g-4">
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a short card.</p>
      </div>
    </div>
  </div>
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content.</p>
      </div>
    </div>
  </div>
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  <div class="col">
    <div :class="[theme === 'dark-mode' ? 'bg-dark text-light' : 'bg-light text-dark']" class="card h-100">
      <img src="..." class="card-img-top" alt="...">
      <div class="card-body">
        <h5 class="card-title">Card title</h5>
        <p class="card-text">This is a longer card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
      </div>
    </div>
  </div>
  
</div>
	</div>
</section>
     </div>
     <!-- gallery section -->
      <div class="row mb-3">
        <section class="py-5" id="gallery-section">
	<div class="container">
		<div class="row justify-content-center text-center mb-2 mb-lg-4">
			<div class="col-12 col-lg-8 col-xxl-7 text-center mx-auto">
				<h2 class="display-5 fw-bold">Our Gallery</h2>
				<p class="lead">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta harum ipsum venenatis metus sem veniam eveniet aperiam suscipit.</p>
			</div>
		</div>
		<div class="row py-3 align-items-center">
			<div class="col-md-6 mt-md-0 mt-4">
				<div class="mb-5 mb-lg-3"><img class="img-fluid" :src="img2"></div>
			</div>
			<div class="col-md-6 ps-md-5">
				<div class="mb-5 mb-lg-3">
					<h4>A Catchy Title</h4>
					<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sapiente accusantium nulla, sequi cupiditate exercitationem sit incidunt rerum explicabo. Soluta beatae esse praesentium exercitationem vero harum pariatur adipisci qui veritatis est!</p>
					<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Soluta harum ipsum venenatis metus sem veniam eveniet aperiam suscipit.</p><a class="btn btn-lg btn-primary" href="">View Gallery</a>
				</div>
			</div>
		</div>
		<div class="row mt-2">
			<div class="col-lg-3 col-md-6">
				<div class="mb-3 mb-lg-0"><img alt="" class="img-fluid" :src="img7"></div>
			</div>
			<div class="col-lg-3 col-md-6">
				<div class="mb-3 mb-lg-0"><img alt="" class="img-fluid" :src="img5"></div>
			</div>
			<div class="col-lg-3 col-md-6">
				<div class="mb-3 mb-lg-0"><img alt="" class="img-fluid" :src="img4"></div>
			</div>
			<div class="col-lg-3 col-md-6">
				<div class="mb-3 mb-lg-0"><img alt="" class="img-fluid" :src="img6"></div>
			</div>
		</div>
	</div>
</section>
      </div>
      <!-- contact section -->
       <div class="row mb-3">
        <section class="py-5">
	<div class="container-fluid p-lg-0">
		<div class="row g-0 align-items-center">
			<div class="col-lg-6">
				<div class="col-lg-8 mx-auto">
					<span class="text-muted">Let's Talk</span>
					<h2 class="display-5 fw-bold">Contact Us</h2>
					<p class="lead">Reach out to us! It doesn't matter whether you just want some fresh mulch, mowing, or a complete landscaping overhaul, </p>
					<p class="lead">Phone: (765) 571-9457</p>
          <p class="lead">Email: wenninglandscape@gmail.com</p>
          <form>
						<div class="row">
							<div class="col-md-12">
								<div class="mb-3">
									<input class="form-control bg-light" placeholder="Your name" type="text">
								</div>
							</div>
							<div class="col-md-12">
								<div class="mb-3">
									<input class="form-control bg-light" placeholder="Your email" type="text">
								</div>
							</div>
							<div class="col-md-12">
								<div class="mb-3">
									<textarea class="form-control bg-light" placeholder="Your message" rows="4"></textarea>
								</div>
							</div>
							<div class="col-md-5">
								<div class="d-grid">
									<button class="btn btn-primary" type="submit">Send message</button>
								</div>
							</div>
						</div>
					</form>
				</div>
			</div>
			<div class="col-lg-6">
				<div class="mt-5 mt-lg-0"><img alt="" class="img-fluid" :src="map"></div>
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
import img1 from './assets/IMG_2143.png'
import img2 from './assets/IMG_5193.png'
import img3 from './assets/IMG_5818.png'
import img4 from './assets/IMG_6828.png'
import img5 from './assets/IMG_6845.png'
import img6 from './assets/IMG_7338.png'
import img7 from './assets/IMG_9873.png'
import map from './assets/map.png'

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
      aboutImage,
      img1,
      img2,
      img3,
      img4,
      img5,
      img6,
      img7,
      map
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