<template>
  <div class="container-fluid background-image">
    <section class="row top-page">
      <div class="col-5">
        <img class="img-fluid" src="src/assets/img/dawson taylor.png" alt="Dawson Taylor" title="Dawson Taylor Logo">
      </div>
      <div class="col-12 col-md-7">
        <p class="arima fs-5 drinks-shadow">We are proud to say that all of our coffee is served fresh via locally owned
          Dawson
          Taylor
          Coffee Roasters.
          We offer 4 different types of drip coffee; light, medium, dark, and decaf. Espresso and decaf espresso are
          also available of course for anything fancier you may desire!<br /><br /></p>
        <p class="arima fs-5 drinks-shadow">Don’t forget our mimosas! Voted best
          mimosas in town, and rightfully so. Not only are the variety of flavors outrageous, but so is the size.
          They’re big and they’re plentiful... </p>
      </div>
      <section class="row mt-3">
        <div class="col-12 col-md-6">

        </div>
        <div class="col-12 col-md-6">
          <div class="d-flex justify-content-around lily">
            <p>Latte</p>
            <p class="hide">*</p>
            <p>Cappuccino</p>
            <p class="hide">*</p>
            <p>Mocha</p>
            <p class="hide">*</p>
            <p>Americano</p>
          </div>
          <div class="d-flex justify-content-between lily">
            <p>Smoothies</p>
            <p class="hide">*</p>
            <p>Red Bull Infusions</p>
            <p class="hide">*</p>
            <p>Bloody Mary</p>
            <p class="hide">*</p>
            <p>Draft Beer</p>
          </div>
        </div>
      </section>
    </section>
  </div>
</template>


<script>
import { AppState } from '../AppState';
import { computed, reactive, onMounted } from 'vue';
export default {
  setup() {
    return {}
  }
};
</script>


<style lang="scss" scoped>
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