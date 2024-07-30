<template>
  <Navbar />
  <main class="container-fluid">
    <div class="row hero-img justify-content-md-end justify-content-center align-items-center">
      <div class="col-md-5 col-10 position-relative">
        <div class="glassCard p-4 text-light" v-for="(paragraph, index) in paragraphs" :key="index"
          :style="{ display: paragraphIndex === index ? 'block' : 'none' }">
          <h4>{{ paragraph }}</h4>
        </div>
      </div>
      <img v-for="(image, index) in images" :key="index" :src="image.src"
        :style="{ display: imageIndex === index ? 'block' : 'none' }"
        class="w-100 h-100 position-absolute top-0 left-0 hero-img-img">
    </div>

    <div class="row text-center text-light p-5 justify-content-center align-items-center">
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light">
          <router-link :to="{ name: 'Bakery' }" class="btn select-borderless text-uppercase">
            <h4>Our Bakery</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </router-link>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light">
          <router-link :to="{ name: 'Shop' }" class="btn select-borderless text-uppercase">
            <h4>Merchandise</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </router-link>
        </div>
      </div>
      <div class="col-md-3 col-10 m-2">
        <div class="card p-4 gc text-light">
          <router-link :to="{ name: 'Contact' }" class="btn select-borderless text-uppercase">
            <h4>Catering</h4>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </router-link>
        </div>
      </div>
    </div>
  </main>

  <Bottom />
</template>

<script>
export default {
  data() {
    return {
      imageIndex: 0,
      images: [
        { src: "/img/latte.jpg" },
        { src: "/img/outside.jpg" },
        { src: "/img/food.png" }
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
    this.startImageRotation();
    this.startParagraphRotation();
  },
  methods: {
    startImageRotation() {
      setInterval(() => {
        this.imageIndex = (this.imageIndex + 1) % this.images.length;
      }, 5000);
    },
    startParagraphRotation() {
      setInterval(() => {
        this.paragraphIndex = (this.paragraphIndex + 1) % this.paragraphs.length;
      }, 5000);
    }
  }
}
</script>

<style>
nav {
  z-index: 3;
  position: relative;
}

.hero-img {
  min-height: 60vh;
  background-position: center;
  background-size: cover;
  background-repeat: none;
  position: relative;
  overflow: hidden;
}

.hero-img-img {
  z-index: 1;
}

.glassCard {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);
  position: absolute;
  top: 50%;
  left: 0;
  right: 0;
  margin: auto;
  transform: translateY(-50%);
  z-index: 2;
}

.gc {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);

}

.imgs {
  height: 200px;
  width: 200px;
  object-fit: cover;
  object-position: center;
}

.purchase-btn {
  position: absolute;
  bottom: -19px;
}

/* @media (max-width: 768px) {
  .hero-img {
    background-image: url("https://images.unsplash.com/photo-1514163061636-02db31852e84?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=774&q=80");
    min-height: 60vh;
    background-position: center;
    background-size: cover;
    background-repeat: none;
  }
} */
</style>
