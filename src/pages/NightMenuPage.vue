<template>
  <NavbarDark />
  <div class="container-fluid bg">
    <section class="row pt-5">
      <div class="col-12 text-center">
        <img class="img-fluid" src="src/assets/img/Coming Soon.png" alt="Coming Soon">
      </div>
    </section>
  </div>
  <BottomDark />
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
.bg {
  background-image: url(https://t3.ftcdn.net/jpg/06/18/16/78/240_F_618167851_rHxwCIwh0EXjUd8NebFhOcHn5cxVw2pk.jpg);
  height: 87vh;
  background-position: center;
  background-size: cover;
}

img {
  height: 70dvh;
  width: auto;
}
</style>