<template>
  <Navbar />
  <div class="container-fluid background-image">
    <section class="row slideshowContent">
      <div class="col-12 image-container d-flex justify-content-center">
        <img v-for="(image, index) in images" :key="index" :src="image.src"
          :style="{ display: imageIndex === index ? 'block' : 'none' }">

        <div class="col-md-5 col-10 position-absolute end-0 top-50 translate-middle-y">
          <div class="glassCard p-4 text-light" v-for="(paragraph, index) in paragraphs" :key="index"
            :style="{ display: paragraphIndex === index ? 'block' : 'none' }">
            <h4>{{ paragraph }}</h4>
          </div>
        </div>
      </div>
    </section>
    <section class="row text-center text-light p-5 justify-content-around align-items-center">
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light line-top line-bottom" data-aos="fade-up">
          <router-link :to="{ name: 'Bakery' }" class="btn select-borderless text-uppercase" title="Bakery Page">
            <h4>Our Bakery</h4>
            <p>We bake 'em fresh everyday so you don't have to. C'mon in for a tasty bite!</p>
          </router-link>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light line-top line-bottom" data-aos="fade-up">
          <router-link :to="{ name: 'Shop' }" class="btn select-borderless text-uppercase" title="Shop Page">
            <h4>Merchandise</h4>
            <p>Looking to take a piece of us home with you? Check out our merch here!</p>
          </router-link>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light line-top line-bottom" data-aos="fade-up">
          <router-link :to="{ name: 'Contact' }" class="btn select-borderless text-uppercase" title="Contact Us Page">
            <h4>Catering</h4>
            <p>You need the eats, we got the treats! We cater perfectly for office meetings.</p>
          </router-link>
        </div>
      </div>
    </section>
  </div>
  <div class="container-fluid">
    <section class="row bground-img justify-content-around py-5">
      <div class="col-10 col-md-6 d-flex align-items-center">
        <p class="fs-5 arima" data-aos="fade-right"><b>Welcome to Goldy's Corner!</b> Where you'll find a leisure place
          to study, hang out
          with
          family
          or friends,
          have a
          work meeting, work out of the office or enjoy the downtown scene. We have proudly serve locally owned Dawson
          Taylor coffee since day one. We provide a variety of homemade treats, drinks, and promote
          local artists and vendors. Local artwork is always on display.
          Thanks for stopping by!</p>
      </div>
      <div class="col-10 col-md-3 second-bg text-center">
        <p class="fw-bold lily" data-aos="fade-down">Coffee Shop • Café • Bakery</p>
        <p data-aos="zoom-in" class="fs-5"> 625 W. Main St., Boise, ID 83702 <br>
          208.433.3934 <br>
          Hours: Monday - Friday: 6:30am - 9:00pm Saturday: 7:00am - 9:00 Sunday: 7am - 7pm <br>
          *Free WIFI <br>
          *Plugins by booths and tables

        </p>
      </div>
    </section>

  </div>
  <Bottom />
</template>





<script>
export default {
  data() {
    return {
      imageIndex: 0,
      images: [
        { src: "src/assets/img/Mimosa.png" },
        { src: "src/assets/img/latte.jpg" },
        { src: "src/assets/img/Cases.png" }
      ],
      textIndex: 0,
      texts: [
        "Happy Hour",
        "Locally Sourced Products",
        "Fresh Baked"
      ],
      paragraphIndex: 0,
      paragraphs: [
        "We offer one of the best happy hours in town! Come in everyday from 5:00pm - 9:00pm for half off any of our award winning mimosas and $1 off any other drink",
        "We take pride in our locally sourced ingredients used in all of our products.",
        "Freshly baked goods daily made by our own in house Blaker."
      ]
    };
  },
  mounted() {
    setInterval(this.nextImage, 4000);
    setInterval(this.nextText, 4000);
    setInterval(this.nextParagraph, 4000)
  },
  methods: {
    nextImage() {
      this.imageIndex = (this.imageIndex + 1) % this.images.length;
    },
    nextText() {
      this.textIndex = (this.textIndex + 1) % this.texts.length;
    },
    nextParagraph() {
      this.paragraphIndex = (this.paragraphIndex + 1) % this.paragraphs.length;
    }
  }
};
</script>


<style lang="scss" scoped>
// .image-container {
//   height: 60vh;
//   overflow: hidden;
// }

// .image-container img {
//   object-fit: cover;
//   height: 100%;
//   width: 100%;
// }

.bground-img {
  background-image: url(src/assets/img/WhiteParchment.png);
  background-position: center;
  background-size: cover;
  box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
}

.second-bg {
  background-color: whitesmoke;
  border-radius: 10px;
  box-shadow: 0px 0px 10px #3c3a3a;
  border: solid thin black;
}

img {
  width: 100vw;
  height: 70vh;
  object-fit: cover;
  overflow: hidden;
  border-radius: 0px 0px 25px 25px;
  box-shadow: 0px 5px var(--bs-success);
}

.glassCard {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);
  margin-right: 3rem;
  margin-top: 5rem;
}

.gc {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: thin solid #0f0f0f42;
  position: relative;
}



.line-bottom::after {
  position: absolute;
  right: 20px;
  bottom: 20px;
  width: 30px;
  height: 30px;
  z-index: 1;
  content: '';
  border-right: 5px solid var(--bs-success);
  border-bottom: 5px solid var(--bs-success);
}

.line-bottom:hover::after {
  position: absolute;
  right: 10px;
  bottom: 10px;
  width: 30px;
  height: 30px;
  z-index: 2;
  content: '';
  border-right: 5px solid var(--bs-success);
  border-bottom: 5px solid var(--bs-success);
  transition: 1s;
}

// .line-bottom:hover::after {
//   position: absolute;
//   left: 10px;
//   top: 10px;
//   width: 30px;
//   height: 30px;
//   z-index: 2;
//   content: '';
//   border-left: 5px solid var(--bs-success);
//   border-top: 5px solid var(--bs-success);
//   transition: 1s;
// }

// .line-top::before {
//   position: absolute;
//   left: 20px;
//   top: 20px;
//   width: 30px;
//   height: 30px;
//   z-index: 1;
//   content: '';
//   border-left: 5px solid var(--bs-success);
//   border-top: 5px solid var(--bs-success);
// }

// .line-top:hover::after {
//   position: absolute;
//   right: 10px;
//   bottom: 10px;
//   width: 30px;
//   height: 30px;
//   z-index: 2;
//   content: '';
//   border-right: 5px solid var(--bs-success);
//   border-bottom: 5px solid var(--bs-success);
//   transition: 1s;
// }

@media (max-width: 768px) {
  .slideshowContent {
    min-height: 60vh;
    background-position: center;
    background-size: cover;
    background-repeat: none;
  }

  .overlay-card {
    width: 90%;
  }
}

nav {
  position: relative;
  z-index: 1000;
}

// Paypal password

// Daddyboiz!</style>
