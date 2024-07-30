<template>
  <Navbar />
  <div class="background-image vh-100 d-flex justify-content-center align-items-center mx-auto">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <div class="pt-5 slideshowContent text-center slide-in underline" v-for="(text, index) in texts" :src="text"
            :key="index" :style="{ display: textIndex === index ? 'block' : 'none' }">
            <p class="fs-1 fw-bold arima">{{ text }} </p>
          </div>
          <div class="slideshowContent text-center" v-for="(paragraph, index) in paragraphs" :src="paragraph"
            :key="index" :style="{ display: paragraphIndex === index ? 'block' : 'none' }">
            <p class="fs-4 fw-bold">{{ paragraph }} </p>
          </div>
        </div>
        <div class="col-md-6">
          <div class="slideshowContent">
            <img v-for="(image, index) in images" :key="index" :src="image.src"
              :style="{ display: imageIndex === index ? 'block' : 'none' }">
          </div>
        </div>
      </div>
    </div>
  </div>
  <Bottom />
</template>

<script>
import Navbar from '../components/Navbar.vue';


export default {
  data() {
    return {
      imageIndex: 0,
      images: [
        { src: "/img/drinks.png" },
        { src: "/img/coffee.png" },
        { src: "/img/food.png" }
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
        "hey hi",
        "whats up",
      ]
      //       HAPPY HOUR...

      // We offer one of the best happy hours in town! Come in everyday from 5:00pm - 9:00pm for half off any of our award winning mimosas and $1 off any other drink

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

<style scoped lang="scss">
img {
  height: 60dvh;
  width: auto;
}

.underline {
  padding: 1rem;
  border-width: 3px;
  border-style: solid;
  border-image: linear-gradient(to bottom, var(--bs-secondary),
      #00000000) 1 100%;
}
</style>