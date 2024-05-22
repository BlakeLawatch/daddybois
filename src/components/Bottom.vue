<template>
    <div class="container-fluid bg-img">
        <section class="row">
            <div class="col-12 col-md-4">
                <p class="text-center text-success p-0">
                    625 W. Main St. | Boise, ID 83702 | P.208.433.3934
                    Copyright © 2024. All Rights Reserved.
                    Website designed by Daddy Bois
                </p>
            </div>
            <div class="col-12 col-md-4 d-flex justify-content-around align-items-center">
                <div>
                    <a target="_blank" href="https://www.instagram.com/goldyscornerboise/"><i
                            class="mdi mdi-instagram fs-2"></i></a>
                    <a target="_blank" href="https://www.facebook.com/goldyscorner"><i
                            class="mdi mdi-facebook fs-2"></i></a>

                </div>
                <div>
                    <a class="fs-4" target="_blank"
                        href="https://www.goldysbreakfastbistro.com/main.html">goldysbreakfastbistro.com</a>

                </div>
            </div>
            <div class="col-12 col-md-4 d-flex justify-content-around align-items-center">

                <router-link :to="{ name: 'Contact' }" class="fs-2 fw-bold btn select-borderless text-success">
                    Catering
                </router-link>

                <router-link :to="{ name: 'Contact' }" class="fs-2 fw-bold btn select-borderless text-success">
                    Contact Us
                </router-link>

            </div>
        </section>
    </div>
</template>


<script>
</script>


<style lang="scss" scoped>
a {
    color: var(--bs-success);
}

a:hover {
    text-shadow: .8px .8px 1px var(--bs-success);
    transition: ease-in-out .4s;
}

.bg-img {
    background-image: url(src/assets/img/Header-Gradient.png);
    background-position: center;
    background-size: cover;
}
</style>