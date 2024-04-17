<template>
  <div class="gallery">
    <div class="container-fluid">
      <div class="row">
        <div class="col-md-12 d-flex flex-wrap justify-content-center py-5">
          <div class="col-md-3 p-3" v-for="(image, index) in images" :key="index">
            <img class="img-fluid max-height selectable" :src="image.src" :alt="image.alt"
              @click="enlargeImage(index)" />
          </div>
        </div>
      </div>
    </div>

    <div v-if="enlargedImageIndex !== -1" class="enlarged" @click="enlargeImage(-1)">
      <img :src="images[enlargedImageIndex].src" :alt="images[enlargedImageIndex].alt" />
    </div>
  </div>
</template>


<script>
import { AppState } from '../AppState';
import { computed, reactive, onMounted } from 'vue';
export default {
  data() {
    return {
      enlargedImageIndex: -1,
      images: [
        { src: "src/assets/img/ShopImages/image 3.png" },
        { src: "src/assets/img/ShopImages/image 4.png" },
        { src: "src/assets/img/ShopImages/image 5.png" },
        { src: "src/assets/img/ShopImages/IMG-2732 1.png" },
        { src: "src/assets/img/ShopImages/IMG-2733 1.png" },
        { src: "src/assets/img/ShopImages/IMG-2734 1.png" },
        { src: "src/assets/img/ShopImages/IMG-2734 2.png" },
        { src: "src/assets/img/ShopImages/IMG-2734 3.png" },
        { src: "src/assets/img/ShopImages/IMG-2734 4.png" },
        { src: "src/assets/img/ShopImages/IMG-2735 1.png" },
      ],
    };
  },
  methods: {
    enlargeImage(index) {
      this.enlargedImageIndex = index;

    }
  }
};
</script>


<style lang="scss" scoped>
.max-height {
  max-height: 25vh;
  max-width: 20vh;
  height: 25vh;
  width: 100%;
  margin-right: 25px;
  filter: drop-shadow(1rem 1rem 10px rgba(255, 255, 255, 0.23));
  transition: transform 0.3s ease-in-out;
}

.max-height:hover {
  transform: scale(1.1);
}

.enlarged {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background: rgba(0, 0, 0, 0.604);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
  // border: 10px solid rgba(0, 0, 0, 0.3);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 999;
}

.enlarged img {
  max-width: 90%;
  max-height: 90%;
  border-radius: 15px;
  filter: drop-shadow(0rem 0rem 15px #0a0a0a);

}

.img-fluid {
  border-radius: 15px;
}

.img-fluid:hover {
  margin-right: 25px;
  filter: drop-shadow(1rem 1rem 10px rgba(0, 0, 0, 0.641));
}

.gallery {
  overflow-x: hidden;
  overflow-y: hidden;
  background-color: #816E5E;
}
</style>