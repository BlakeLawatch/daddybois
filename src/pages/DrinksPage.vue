<template>
  <Navbar />
  <div class="container-fluid background-image">
    <section class="row top-page mb-5">
      <div class="col-12 col-md-5 text-center">
        <img src="/img/dawson_taylor.jpg" alt="Dawson Taylor" title="Dawson Taylor Logo">
      </div>
      <div data-aos="fade-left" class="col-12 col-md-7">
        <p class="arima fs-5 drinks-shadow">We are proud to say that all of our coffee is served
          fresh via locally owned
          Dawson
          Taylor
          Coffee Roasters.
          We offer 4 different types of drip coffee; light, medium, dark, and decaf. Espresso and decaf espresso are
          also available of course for anything fancier you may desire!<br /><br /></p>
        <p class="arima fs-5 drinks-shadow">Don’t forget our mimosas! Voted best
          mimosas in town, and rightfully so. Not only are the variety of flavors outrageous, but so is the size.
          They’re big, they’re plentiful, and they're 50% off during happy hour <i>5:00 pm - 9:00 pm</i> </p>
      </div>
    </section>
    <section class="row mt-3 justify-content-around pb-5">
      <div class="col-11 col-md-4 bg-color p-5">
        <div class="d-flex justify-content-between mx-2">
          <p class="fs-2 fw-bold">Mimosa</p>
          <p class="fs-2 fw-bold" data-aos="fade-left">...$12.95</p>
        </div>
        <div class="d-flex justify-content-between mx-2">
          <p class="fs-2 fw-bold">Mimosa Flight</p>
          <p class="fs-2 fw-bold" data-aos="fade-left">...$14.95</p>
        </div>
        <div class="d-flex justify-content-between">

          <div>
            <p class="mb-0">Traditional</p>
            <p class="mb-0">Strawberry</p>
            <p class="mb-0">Sunrise <br> (Mango, Guava, Orange, <br> touch of Cranberry)</p>
            <p class="mb-0"></p>
          </div>
          <div>
            <p class="mb-0">Mango</p>
            <p class="mb-0">Berries n Bubbles</p>
            <p class="mb-0">Lavender</p>
            <p class="mb-0">...and so many more</p>
          </div>
        </div>
      </div>
      <div class="col-12 col-md-6 hide">
        <div class="d-flex justify-content-around lily">
          <!-- <p class="btn fs-2" data-bs-toggle="modal" data-bs-target="#latte">Latte</p> -->
          <p>Latte</p>
          <p>*</p>
          <p>Cappuccino</p>
          <p>*</p>
          <p>Mocha</p>
          <p>*</p>
          <p>Americano</p>
        </div>
        <div class="d-flex justify-content-between lily">
          <p>Smoothies</p>
          <p>*</p>
          <p>Red Bull Infusions</p>
          <p>*</p>
          <p>Bloody Mary</p>
          <p>*</p>
          <p>Draft Beer</p>
        </div>
      </div>
    </section>
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
.bg-color {
  background-color: #7a883d;
  border-radius: 40% 15% 40% 25%;
}

img {
  height: 40vh;
  width: auto
}

@media(max-width: 767px) {
  img {
    display: none;
  }

  @media(max-width: 676px) {
    .hide {
      visibility: hidden;
    }
  }


}
</style>