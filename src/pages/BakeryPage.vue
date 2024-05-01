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
    <section class="row mt-5">
      <div class="col-4">
        <h3 class="text-center">Muffins...$3.25</h3>
      </div>
      <div class="col-4">
        <h3 class="text-center">Savory</h3>
      </div>
      <div class="col-4">
        <h3>Cookies...$1.75</h3>
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


<style lang="scss" scoped></style>