<template>
  <nav class="navbar navbar-expand-sm navbar-dark px-3 bg-img">
    <router-link class="navbar-brand d-flex" :to="{ name: 'Home' }">
      <div class="logo d-flex flex-column align-items-center position-relative">
        <img alt="logo" class="" src="src/assets/img/GOLDYS-LOGO_FINAL[1].png" height="180" />
      </div>
    </router-link>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText"
      aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarText">
      <ul class="navbar-nav">
        <li>
          <router-link :to="{ name: 'Bakery' }" class="btn text-success lighten-30 selectable text-uppercase">
            Bakery
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'Drinks' }" class="btn text-success lighten-30 selectable text-uppercase">
            Drinks
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'Shop' }" class="btn text-success lighten-30 selectable text-uppercase">
            Shop
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'NightMenu' }" class="btn text-success lighten-30 selectable text-uppercase">
            Night Menu
          </router-link>
        </li>
        <li>
          <router-link :to="{ name: 'Contact' }" class="btn text-success lighten-30 selectable text-uppercase">
            Contact Us
          </router-link>
        </li>
      </ul>

    </div>
  </nav>
</template>

<script>
import { computed, onMounted, ref } from 'vue';
import { loadState, saveState } from '../utils/Store.js';
export default {
  setup() {

    const theme = ref(loadState('theme') || 'light')

    onMounted(() => {
      document.documentElement.setAttribute('data-bs-theme', theme.value)
    })

    return {
      theme,
      toggleTheme() {
        theme.value = theme.value == 'light' ? 'dark' : 'light'
        document.documentElement.setAttribute('data-bs-theme', theme.value)
        saveState('theme', theme.value)
      }
    }
  },
}
</script>

<style scoped>
.bg-img {
  background-image: url(src/assets/img/Header-Gradient.png);
  background-position: center;
  background-size: contain;
}

.logo {
  margin-top: 120px;
}

a:hover {
  text-decoration: none;
}

.nav-link {
  text-transform: uppercase;
}

.navbar-nav .router-link-exact-active {
  border-bottom: 2px solid var(--bs-success);
  border-bottom-left-radius: 0;
  border-bottom-right-radius: 0;
}

@media screen and (min-width: 576px) {
  nav {
    height: 64px;
  }
}
</style>
