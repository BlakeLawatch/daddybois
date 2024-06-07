<template>
  <div class="nav-container col-md-12">
    <Navbar />
  </div>
  <main class="container-fluid background-image">
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
        <img class="itemImage rounded" src="src\assets\img\ShopImages\white.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\corner.png" alt="">
        <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
      </div>

      <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-3">
        <img class="itemImage rounded" src="src\assets\img\ShopImages\1.png" alt="">
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

</script>


<style lang="scss" scoped>
.nav-container {
  position: relative;
  z-index: 1000;
  /* Increased z-index */
}

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

.bground-img {
  background-image: url(src/assets/img/WhiteParchment.png);
  background-position: center;
  background-size: cover;
  box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
}
</style>