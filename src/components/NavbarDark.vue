<template>
    <nav class="navbar navbar-expand-sm px-3 bg-img py-4">
        <router-link class="navbar-brand d-flex" :to="{ name: 'Home' }">
            <div class="logo-space d-flex flex-column align-items-center">
                <img alt="logo" class="logo" src="src/assets/img/NightLogo.png" />
                <!-- <img alt="logo" class="logo" src="src/assets/img/NightLogoWhite.png" /> -->
            </div>
        </router-link>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarText"
            aria-controls="navbarText" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarText">
            <ul class="navbar-nav">
                <li>
                    <router-link :to="{ name: 'Bakery' }" class="btn border-side text-color select text-uppercase">
                        Bakery
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ name: 'Drinks' }" class="btn border-side text-color select text-uppercase">
                        Drinks
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ name: 'Shop' }" class="btn border-side text-color select text-uppercase">
                        Shop
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ name: 'NightMenu' }" class="btn border-side text-color select text-uppercase">
                        Night Menu
                    </router-link>
                </li>
                <li>
                    <router-link :to="{ name: 'Contact' }" class="btn select-borderless text-color text-uppercase">
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
    background: linear-gradient(#313163, #35c4ef);
    /* background: linear-gradient(#35c4ef, #313163); */
}

.text-color {
    color: #f0c051;
}

.logo-space {
    margin-top: 120px;
}

@media(max-width: 767px) {
    .logo-space {
        margin-top: 0;
    }
}

.logo {
    height: 25vh;
    width: auto;
    filter: drop-shadow(2px 2px 2px #200606);
}

@media (max-width: 767px) {
    .logo {
        height: 15vh;
        width: auto;
        filter: drop-shadow(2px 2px 2px #200606);

    }
}

a:hover {
    text-decoration: none;
}

.nav-link {
    text-transform: uppercase;
}

.navbar-nav .router-link-exact-active {
    border-bottom: 2px solid #f0c051;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
}

@media screen and (min-width: 576px) {
    nav {
        height: 64px;
    }
}

.border-side {
    border-right: thin dashed #f0c051;
    border-radius: 0;
}

@media(max-width: 767px) {
    .border-side {
        border-right: none;
    }
}

.select {
    font-size: 1rem;
}

.select:hover {
    text-shadow: 1px 1px 2px #824020;
    transition: ease-in-out .3s;
    border-right: thin dashed #f0c051;
    border-radius: 0;
}

.select-borderless {
    font-size: 1rem;
}

.select-borderless:hover {
    text-shadow: 1px 1px 2px #824020;
    transition: ease-in-out .3s;

}
</style>