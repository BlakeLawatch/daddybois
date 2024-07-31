<template>
    <div class="container-fluid bg-img">
        <section class="row">
            <div class="col-12 col-md-4 d-flex">
                <p class="text-center text-success pb-0 pt-1">
                    625 W. Main St. | Boise, ID 83702 | P.208.433.3934
                    Copyright © 2024. All Rights Reserved.
                    Website designed by <a href="https://www.linkedin.com/in/jacob-winfrey-a9a2a4280/" target="_blank"
                        title="Go to Jake's Linkedin">Jake</a> &
                    <a href="https://www.linkedin.com/in/blakelawatch/" target="_blank"
                        title="Go to Blake's Linkedin">Blake</a>
                </p>
            </div>
            <div class="col-12 col-md-8 d-flex justify-content-around align-items-center">
                <div>
                    <a target="_blank" href="https://www.instagram.com/goldyscornerboise/"><i
                            class="mdi mdi-instagram fs-2" title="Instagram"></i></a>
                    <a target="_blank" href="https://www.facebook.com/goldyscorner"><i class="mdi mdi-facebook fs-2"
                            title="Facebook"></i></a>

                </div>
                <div>
                    <a class="fs-4" target="_blank" href="https://www.goldysbreakfastbistro.com/main.html"
                        title="Goldys Breakfast Bistro Website">goldysbreakfastbistro.com</a>

                </div>
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
    background-image: url(/img/Header-Gradient.jpg);
    background-position: center;
    background-size: cover;
}
</style>