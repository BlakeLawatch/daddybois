<template>
  <NavbarDark />
  <div class="container-fluid bg">
    <section class="row pt-5">
      <div class="col-12 text-center">
        <img class="img-fluid" src="/img/Coming_Soon-Def.png" alt="Coming Soon">
      </div>
    </section>
  </div>
  <BottomDark />
</template>


<script>
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
  animation-name: spin;
  animation-duration: 10000ms;
  animation-iteration-count: infinite;
  animation-timing-function: linear;
}

@keyframes spin {
  from {
    transform: rotate(0deg);
  }

  to {
    transform: rotate(360deg);
  }
}
</style>