<template>
    <div class="container-fluid">
        <section class="row">
            <div class="col-4">
                <p>
                    625 W. Main St. | Boise, ID 83702 | P.208.433.3934
                    Copyright © 2024. All Rights Reserved.
                    Website designed by Daddy Bois
                </p>
            </div>
            <div class="col-4">
                <a target="_blank" href="https://www.instagram.com/goldyscornerboise/"><i
                        class="mdi mdi-instagram"></i></a>
                <a target="_blank" href="https://www.facebook.com/goldyscorner"><i class="mdi mdi-facebook"></i></a>
                <a target="_blank" href="https://www.goldysbreakfastbistro.com/main.html">Goldys
                    Breakfast Bistro</a>
            </div>
            <div class="col-4">
                <router-link :to="{ name: 'Contact' }" class="btn select-borderless text-success">
                    Catering
                </router-link>
                <router-link :to="{ name: 'Contact' }" class="btn select-borderless text-success">
                    Contact Us
                </router-link>
            </div>
        </section>
    </div>
</template>


<script>
</script>


<style lang="scss" scoped></style>