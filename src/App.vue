<template>
  <header>
    <Navbar />
  </header>
  <main>
    <router-view />
  </main>
  <footer class="bg-dark text-light">
    Made with 💖 by Daddy Boiz
  </footer>
</template>

<script>
import { computed } from 'vue'
import { AppState } from './AppState'
import Navbar from './components/Navbar.vue'

export default {
  setup() {
    return {
      appState: computed(() => AppState)
    }
  },
  components: { Navbar }
}
</script>
<style lang="scss">
@import "./assets/scss/main.scss";
@import url('https://fonts.googleapis.com/css2?family=Frijole&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Emilys+Candy&family=Frijole&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Emilys+Candy&family=Frijole&family=Henny+Penny&display=swap');

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

.frijole {
  font-family: "Frijole", system-ui;
  font-weight: 400;
  font-style: normal;
}

.candy {
  font-family: "Emilys Candy", serif;
  font-weight: 400;
  font-style: normal;
}

.penny {
  font-family: "Henny Penny", system-ui;
  font-weight: 400;
  font-style: normal;
}
</style>
