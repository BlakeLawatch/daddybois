<template>
  <Navbar />
  <div class="container-fluid background-image">
    <section class="row top-page">
      <div class="d-flex justify-content-center">
        <iframe class="videos"
          src="https://www.youtube.com/embed/UGvsHQ55Kng?si=6hyjMkzFB3jyC8jx?rel=0&amp;autoplay=1&mute=1;&loop=1&list=PL0pkHXBEYrYtGm8Ssy4Ko61RBQyu_ry_n;"
          title="YouTube video player" frameborder="0" allow="autoplay" referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen></iframe>

      </div>
      <!-- width="1155" height="650" -->
    </section>
    <section class="row mt-5 text-center" data-aos="zoom-in-down">
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Muffins</h3>
        <p class="arima">Blueberry</p>
        <p class="arima">Date Bran</p>
        <p class="arima">Apple Walnut</p>
        <p class="arima">Bread Pudding</p>
      </div>
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Savory</h3>
        <p class="arima">Denver Quiche</p>
        <p class="arima">Goat Cheese Quiche</p>
        <p class="arima">Bacon Casserole</p>
        <p class="arima">Veggie Casserole</p>
        <p class="arima">Chicken Pot Pie</p>
        <p class="arima">Bacon Sandwich</p>
        <p class="arima">Veggie Sandwich</p>
        <p class="arima">* Breakfast Burritos</p>
      </div>
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Misc</h3>
        <p class="arima">Cinnamon Roll</p>
        <p class="arima">Caramel Roll</p>
        <p class="arima">Coffee Cake</p>
        <p class="arima">Fruit Parfait</p>
        <p class="arima">Carrot Cake</p>
      </div>
    </section>
    <section class="row text-center py-5" data-aos="zoom-in-up">
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Scones</h3>
        <p class="arima">Blueberry-lemon</p>
        <p class="arima">* Raspberry-White Chocolate</p>
        <p class="arima">* Pumpkin-Maple Glaze</p>
        <p class="arima">* Snickerdoodle</p>
      </div>
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Cookies</h3>
        <p class="arima">Chocolate Chip</p>
        <p class="arima">Coconut Macaroon</p>
        <p class="arima">Peanut Butter</p>
      </div>
      <div class="col-12 col-md-4">
        <h3 class="arima fw-bold">Breads</h3>
        <p class="arima">Lemon</p>
        <p class="arima">Chocolate Zucchini</p>
        <p class="arima">Pumpkin</p>
        <p class="arima">Banana</p>
      </div>
    </section>
    <div class="col-12">
      <p class="text-center arima fs-5 py-2"><i>* subject to seasonal or daily changes</i></p>
    </div>
  </div>
  <Bottom />
</template>


<script>


export default {
  setup() {


    return {

    }

  }

};
</script>


<style lang="scss" scoped>
p {
  margin-bottom: 0;
  font-size: 22px;
  font-weight: 550;
}

.videos {
  height: 90dvh;
  width: 72.4dvw;
}


@media(max-width: 767px) {
  .videos {
    height: 28.6dvh;
    width: 90dvw;

  }
}

@media(min-width: 1600px) {
  .videos {
    height: 80dvh;
    width: 76.4dvw;

  }
}
</style>