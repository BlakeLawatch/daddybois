<template>
  <Navbar />
  <main class="container-fluid background-image vh-100">
    <div class="row justify-content-center align-items-center slideshowContent">
      <div class="col-md-12 position-relative image-container">
        <img v-for="(image, index) in images" :key="index" :src="image.src"
          :style="{ display: imageIndex === index ? 'block' : 'none' }" class="w-100 h-100">

        <div class="col-md-5 col-10 position-absolute end-0 top-50 translate-middle-y">
          <div class="glassCard p-4 text-light" v-for="(paragraph, index) in paragraphs" :key="index"
            :style="{ display: paragraphIndex === index ? 'block' : 'none' }">
            <h4>{{ paragraph }}</h4>
          </div>
        </div>
      </div>
    </div>
    <div class="row text-center text-light p-5 justify-content-center align-items-center">
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 bg">
          <h4>Our Bakery</h4>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 bg">
          <h4>Merchandise</h4>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 bg">
          <h4>Catering</h4>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
        </div>
      </div>
    </div>
  </main>
  <Bottom />
</template>





<script>
import Navbar from '../components/Navbar.vue';
export default {
  data() {
    return {
      imageIndex: 0,
      images: [
        { src: "src/assets/img/latte.jpg" },
        { src: "src/assets/img/outside.jpg" },
        { src: "src/assets/img/food.png" }
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
        "Locally sourced ingredients for all our products.",
        "Freshly baked goods daily."
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
.image-container {
  height: 60vh;
  overflow: hidden;
}

.image-container img {
  object-fit: cover;
  height: 100%;
  width: 100%;
}

.glassCard {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);
}

.bg {
  background-color: #8e5226;
}

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
</style>
