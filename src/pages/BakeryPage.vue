<template>
  <Navbar />
  <div class="container-fluid background-image">
    <section class="row top-page">
      <!-- <video autoplay muted loop id="myVideo">
        <source src="" type="video/mp4">
      </video> -->
      <div class="d-flex justify-content-center">
        <iframe width="1600" height="800"
          src="https://www.youtube.com/embed/UGvsHQ55Kng?si=6hyjMkzFB3jyC8jx?rel=0&amp;autoplay=1&mute=1;&loop=1&list=PLbpi6ZahtOH6PVhBTPhS6iDUkFGJBeH9g;"
          title="YouTube video player" frameborder="0" allow="autoplay" referrerpolicy="strict-origin-when-cross-origin"
          allowfullscreen></iframe>

      </div>
    </section>
    <section class="row mt-5 text-center" data-aos="zoom-in-down">
      <div class="col-4">
        <h3 class="arima fw-bold">Muffins ...$3.25</h3>
        <p class="arima">Blueberry</p>
        <p class="arima">Date Bran</p>
        <p class="arima">Apple Walnut</p>
        <p class="arima">Bread Pudding</p>
      </div>
      <div class="col-4">
        <h3 class="arima fw-bold">Savory</h3>
        <p class="arima">Denver Quiche ...$5.75</p>
        <p class="arima">Goat Cheese Quiche ...$5.75</p>
        <p class="arima">Bacon Casserole ...$7.75</p>
        <p class="arima">Veggie Casserole ...$7.75</p>
        <p class="arima">Chicken Pot Pie ...$7.00</p>
        <p class="arima">Bacon Sandwich ...$5.50</p>
        <p class="arima">Veggie Sandwich ...$5.50</p>
        <p class="arima">* Breakfast Burritos ...$7.95</p>
      </div>
      <div class="col-4">
        <h3 class="arima fw-bold">Misc</h3>
        <p class="arima">Cinnamon Roll ...$5.75</p>
        <p class="arima">Caramel Roll ...$6.00</p>
        <p class="arima">Coffee Cake ...$4.75</p>
        <p class="arima">Fruit Parfait ...$5.50</p>
        <p class="arima">Carrot Cake ...$3.50</p>
      </div>
    </section>
    <section class="row text-center py-5" data-aos="zoom-in-up">
      <div class="col-4">
        <h3 class="arima fw-bold">Scones ...$4.25</h3>
        <p class="arima">Blueberry-lemon</p>
        <p class="arima">* Raspberry-White Chocolate</p>
        <p class="arima">* Pumpkin-Maple Glaze</p>
        <p class="arima">* Snickerdoodle</p>
      </div>
      <div class="col-4">
        <h3 class="arima fw-bold">Cookies ...$1.75</h3>
        <p class="arima">Chocolate Chip</p>
        <p class="arima">Coconut Macaroon</p>
        <p class="arima">Peanut Butter</p>
      </div>
      <div class="col-4">
        <h3 class="arima fw-bold">Breads ...$3.50</h3>
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
</style>