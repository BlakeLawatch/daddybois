<template>
  <!-- <header>
    <Navbar />
  </header> -->
  <main>
    <router-view />
  </main>
  <!-- <footer>
    <Footer />
  </footer> -->
</template>

<script>
import { computed } from 'vue'
import { AppState } from './AppState'
import Navbar from './components/Navbar.vue'


export default {
  setup() {
    return {
      appState: computed(() => AppState),
    }
  },
  // components: { Navbar }
}
</script>
<style lang="scss">
@import "./assets/scss/main.scss";

@import url('https://fonts.googleapis.com/css2?family=Arima:wght@100..700&family=Emilys+Candy&family=Frijole&family=Henny+Penny&family=Lily+Script+One&family=Rhodium+Libre&display=swap');

:root {
  --main-height: calc(100vh - 32px - 64px);
}


footer {
  display: grid;
  place-content: center;
  height: 32px;
}

.background-image {
  background-image: url('src/assets/img/ParchmentPaper3.png');
  background-size: cover;
  background-position: center;
}

.top-page {
  padding-top: 20vh;
}

.rhodium {
  font-family: "Rhodium Libre", serif;
  font-weight: 400;
  font-style: normal;
}

.lily {
  font-family: "Lily Script One", system-ui;
  font-weight: 400;
  font-size: 1.7rem;
  font-style: normal;
}



.arima {
  font-family: "Arima", system-ui;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
}

.select-borderless {
  font-size: 1rem;
}

.select-borderless:hover {
  text-shadow: 1px 1px 2px #824020;
  transition: ease-in-out .3s;

}
</style>
