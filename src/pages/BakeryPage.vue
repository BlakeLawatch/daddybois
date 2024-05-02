<template>
  <div class="container-fluid background-image">
    <section class="row top-page">
      <div class="d-flex justify-content-center">
        <iframe width="500" height="315" src="https://www.youtube.com/embed/ZpUYjpKg9KY?si=_gluCSkjwvU8ozDb"
          title="YouTube video player" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
          referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

      </div>
    </section>
    <section class="row mt-5 text-center">
      <div class="col-4">
        <h3>Muffins ...$3.25</h3>
        <p>Blueberry</p>
        <p>Date Bran</p>
        <p>Apple Walnut</p>
        <p>Bread Pudding</p>
      </div>
      <div class="col-4">
        <h3>Savory</h3>
        <p>Denver Quiche ...$5.75</p>
        <p>Goat Cheese Quiche ...$5.75</p>
        <p>Bacon Casserole ...$7.75</p>
        <p>Veggie Casserole ...$7.75</p>
        <p>Chicken Pot Pie ...$7.00</p>
        <p>Bacon Sandwich ...$5.50</p>
        <p>Veggie Sandwich ...$5.50</p>
        <p>Breakfast Burritos ...$7.95</p>
      </div>
      <div class="col-4">
        <h3>Breads ...$3.50</h3>
        <p>Lemon</p>
        <p>Chocolate Zucchini</p>
        <p>Pumpkin</p>
        <p>Banana</p>
      </div>
    </section>
    <section class="row text-center pt-5">
      <div class="col-4">
        <h3>Scones ...$4.25</h3>
        <p>Blueberry-lemon</p>
        <p>Raspberry-White Chocolate</p>
        <p>Pumpkin-Maple</p>
        <p>Snickerdoodle</p>
      </div>
      <div class="col-4">
        <h3>Cookies ...$1.75</h3>
        <p>Chocolate Chip</p>
        <p>Coconut Macaroon</p>
        <p>Peanut Butter</p>
      </div>
      <div class="col-4">
        <h3>Misc</h3>
        <p>Cinnamon Roll ...$5.75</p>
        <p>Caramel Roll ...$6.00</p>
        <p>Coffee Cake ...$4.75</p>
        <p>Fruit Parfait ...$5.50</p>
        <p>Carrot Cake ...$3.50</p>
        <!-- Cinnamon Rolls ...$5.75
Caramel Rolls ...$6.00
Coffee Cake ...$4.75
Fruit Parfait ...$5.50
Carrot Cake ...$3.50 -->
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
p {
  margin-bottom: 0;
}
</style>