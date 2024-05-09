<template>
  <div class="container-fluid background-image">
    <section class="row top-page">
      <div class="col-5">
        <img class="img-fluid" src="src/assets/img/dawson taylor.png" alt="Dawson Taylor" title="Dawson Taylor Logo">
      </div>
      <div class="col-7">
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
// .drinks-shadow {
//   text-shadow: none;
// }

// .drinks-shadow:hover {
//   text-shadow: 1px 1px 3px #7a883c;
//   transition: ease-in-out .5s;
// }</style>