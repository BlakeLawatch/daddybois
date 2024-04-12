<template>
  <div>Blake Likes Donkey Dong</div>
</template>


<script>





export default {
  setup() {
    // Aos.init();
    return {

    }
      ;
  },
}
</script>


<style scoped lang="scss">
.bg-image {
  background-color: #816E5E;
  height: 90svh;
}





.cards {
  height: 30vh;
  color: #361112c7;
  background-color: #e4a960;
  border-radius: 15px;
  padding-top: .5rem;
  margin-top: 2rem;
  margin-bottom: 5rem;
  align-items: center;
}

.cards:hover {
  background-color: #624120;
  color: #e4a960;
  transition: ease-in-out 1s;
  animation-name: card;
  animation-duration: 1.5s;
  // animation-delay: ;

}

@media(max-width: 767px) {
  .cards {
    margin-bottom: 1rem;
  }
}

@keyframes card {
  from {
    transform: scaleY(100%);

  }

  50% {
    transform: scaleY(110%);
  }

  to {
    transform: scaleY(100%);
  }
}

.gradient-text {
  font-family: "El Messiri", sans-serif;
  filter: drop-shadow(5px 5px 5px black);
  font-size: 3.5rem;
  background-image: linear-gradient(to right, #361112, #e4a960, #ddbf99);
  background-size: 100%;
  background-repeat: repeat;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-background-clip: text;
  -moz-text-fill-color: transparent;
}

@media (max-width: 767px) {
  .slideshow-view {
    visibility: hidden;
    display: none;

  }
}

.carousel-view {
  height: 30vh;
  width: 80vw;
}

@media (min-width: 767px) {
  .carousel-view {
    visibility: hidden;
    display: none;
  }
}

.border-style {
  box-shadow: inset 0px 6px 10px #ffffff;
}
</style>
