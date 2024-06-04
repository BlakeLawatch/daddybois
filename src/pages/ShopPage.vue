<template>
  <Navbar />
  <!-- <div class="background-image vh-100 gallery">
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
  </div> -->
  <!-- <div class="background-image top-page">
    <div class="container-fluid">
      <div class="row justify-content-around">
        <div class="col-12 col-md-3">
          <div class="item-card bg-success">
            <img src="src/assets/img/ShopImages/image 3.png" alt="item Image">
            <h2 class="item-title text-white">16oz Mug (Orange)</h2>
            <p class="item-price">$19.99</p>
            <button class="btn btn-primary">Add to Cart</button>
          </div>
        </div>
        <div class="col-12 col-md-3">
          <div class="item-card bg-success">
            <img src="src/assets/img/ShopImages/image 4.png" alt="item Image">
            <h2 class="item-title text-white">12oz Mug (Clear)</h2>
            <p class="item-price">$24.99</p>
            <button class="btn btn-primary">Add to Cart</button>
          </div>
        </div>
        <div class="col-12 col-md-3">
          <div class="item-card bg-success">
            <img src="src/assets/img/ShopImages/IMG-2732 1.png" alt="item Image">
            <h2 class="item-title text-white">16oz Mug (Grey/Orange)</h2>
            <p class="item-price">$14.99</p>
            <button class="btn btn-primary">Add to Cart</button>
          </div>
        </div>
        <div class="row justify-content-around">
          <div class="col-12 col-md-3">
            <div class="item-card bg-success">
              <img src="src/assets/img/ShopImages/IMG-2732 1.png" alt="item Image">
              <h2 class="item-title text-white">16oz Mug (Grey/Orange)</h2>
              <p class="item-price">$14.99</p>
              <button class="btn btn-primary">Add to Cart</button>
            </div>
          </div>
          <div class="col-12 col-md-3">
            <div class="item-card bg-success">
              <img src="src/assets/img/ShopImages/IMG-2732 1.png" alt="item Image">
              <h2 class="item-title text-white">16oz Mug (Grey/Orange)</h2>
              <p class="item-price">$14.99</p>
              <button class="btn btn-primary">Add to Cart</button>
            </div>
          </div>
          <div class="col-12 col-md-3">
            <div class="item-card bg-success">
              <img src="src/assets/img/ShopImages/IMG-2732 1.png" alt="item Image">
              <h2 class="item-title text-white">16oz Mug (Grey/Orange)</h2>
              <p class="item-price">$14.99</p>
              <button class="btn btn-primary">Add to Cart</button>
            </div>
          </div>

        </div>
      </div>
    </div>
  </div> -->

  <main class="container-fluid">
    <div class="row p-5 justify-content-center">
      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\black.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\glass.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\grey.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\orange.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\red.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\white.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\red.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\gift.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

    </div>
  </main>
  <Bottom />
</template>


<script>
import Navbar from '../components/Navbar.vue';


// import { AppState } from '../AppState';
// import { computed, reactive, onMounted } from 'vue';
// export default {
//   data() {
//     return {
//       enlargedImageIndex: -1,
//       images: [
//         { src: "src/assets/img/ShopImages/image 3.png" },
//         { src: "src/assets/img/ShopImages/image 4.png" },
//         { src: "src/assets/img/ShopImages/image 5.png" },
//         { src: "src/assets/img/ShopImages/IMG-2732 1.png" },
//         { src: "src/assets/img/ShopImages/IMG-2733 1.png" },
//         { src: "src/assets/img/ShopImages/IMG-2734 1.png" },
//         { src: "src/assets/img/ShopImages/IMG-2734 2.png" },
//         { src: "src/assets/img/ShopImages/IMG-2734 3.png" },
//         { src: "src/assets/img/ShopImages/IMG-2734 4.png" },
//         { src: "src/assets/img/ShopImages/IMG-2735 1.png" },
//       ],
//     };
//   },
//   methods: {
//     enlargeImage(index) {
//       this.enlargedImageIndex = index;

//     }
//   }
// };
</script>


<style lang="scss" scoped>
.nav {
  z-index: 1;
}

.item-card {
  border: 1px solid #ddd;
  border-radius: 5px;
  padding: 20px;
  margin-bottom: 20px;
}

.item-card img {
  max-width: 300px;
  max-height: 300px;
  height: auto;
}

.item-title {
  font-weight: bold;
}

.item-price {
  color: #ffffff;
}

.itemImage {
  height: 200px;
  width: 200px;
  object-fit: cover;
  object-position: center;
}

.glassCard {
  background: rgba(15, 15, 15, 0.354);
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);
}

.purchase-btn {
  position: absolute;
  bottom: -19px;
  /* left: 76px; */
}

// .max-height {
//   max-height: 25vh;
//   max-width: 20vh;
//   height: 25vh;
//   width: 100%;
//   margin-right: 25px;
//   filter: drop-shadow(1rem 1rem 10px rgba(255, 255, 255, 0.23));
//   transition: transform 0.3s ease-in-out;
// }

// .max-height:hover {
//   transform: scale(1.1);
// }

// .enlarged {
//   position: fixed;
//   top: 0;
//   left: 0;
//   width: 100vw;
//   height: 100vh;
//   background: rgba(0, 0, 0, 0.604);
//   border-radius: 16px;
//   box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
//   backdrop-filter: blur(5px);
//   -webkit-backdrop-filter: blur(5px);
//   // border: 10px solid rgba(0, 0, 0, 0.3);
//   display: flex;
//   justify-content: center;
//   align-items: center;
//   z-index: 999;
// }

// .enlarged img {
//   max-width: 90%;
//   max-height: 90%;
//   border-radius: 15px;
//   filter: drop-shadow(0rem 0rem 15px #0a0a0a);

// }

// .img-fluid {
//   border-radius: 15px;
// }

// .img-fluid:hover {
//   margin-right: 25px;
//   filter: drop-shadow(1rem 1rem 10px rgba(0, 0, 0, 0.641));
// }

// .gallery {
//   overflow-x: hidden;
//   overflow-y: hidden;
//   background-color: #816E5E;
// }</style>