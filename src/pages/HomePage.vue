<template>
  <div class="background-image vh-100 d-flex justify-content-center align-items-center mx-auto">
    <div class="container">
      <div class="row">
        <div class="col-md-6">
          <div class="text mx-md-auto pt-5 slideshowContent slideshowContent" v-for="(text, index) in texts" :src="text"
            :key="text" :style="{ display: textIndex === index ? 'block' : 'none' }">
            <p>{{ text }} </p>
          </div>
          <!-- <div class="col-md-6">
          <div class="text mx-md-auto pt-5">
            <h1>LOCALLY OWNED...</h1>
            <b>Both Goldy's Corner and Goldys Breakfast Bistro are owned by the same family. Supporting local as much as
              possible is very important to us as we source as many products locally as we can.</b>
          </div> -->
        </div>
        <div class="col-md-6">
          <div class="slideshowContent slideshowContent" style="max-width:500px">
            <img v-for="(image, index) in images" :key="index" :src="image.src" style="width:100%"
              :style="{ display: imageIndex === index ? 'block' : 'none' }">
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      imageIndex: 0,
      images: [
        { src: "src/assets/img/coffee.png" },
        { src: "src/assets/img/food.png" },
        { src: "src/assets/img/drinks.png" }
      ],
      textIndex: 0,
      texts: [
        "butt",
        "weiner",
        "boobs"
      ]
    };
  },
  mounted() {
    setInterval(this.nextImage, 4000);
    setInterval(this.nextText, 4000)
  },
  methods: {
    nextImage() {
      this.imageIndex = (this.imageIndex + 1) % this.images.length;
    },
    nextText() {
      this.textIndex = (this.textIndex + 1) % this.texts.length;
    }
  }
};
</script>

<style scoped lang="scss">
.background-image {
  background-image: url('C:\\Users\\jacob\\source\\codeworks\\MyStuff\\goldys_corner\\src\\assets\\img\\ParchmentPaper3.png');
  background-size: cover;
  background-position: center;
}

.text {
  max-width: 400px;
}
</style>