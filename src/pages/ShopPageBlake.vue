<template>
    <div class="nav-container col-md-12">
        <Navbar />
    </div>
    <main class="container-fluid background-image top-page">
        <section class="row">

        </section>

        <section class="row p-5 justify-content-center">

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BrownMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueDarkblueMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ClearMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GreyOrangeMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GroundCoffeeBeans.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WholeCoffeeBeans.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Beanie.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>


            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayWomansShirt.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PinkWomansShirt.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Chapstick.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GiftCard.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PurpleWomensShirt.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayMensShirt.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMensShirt.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ChampagneGlass.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WaterBottle.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Tumbler.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GoldysSpice.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/CornerMug.png" alt="">
                <button class="btn glassCard text-light purchase-btn">Add To Cart</button>
            </div>

        </section>
    </main>
    <Bottom />
</template>


<script>
import { onMounted } from 'vue';

export default {
    setup() {


        return {

        }
    }
}


</script>


<style lang="scss" scoped>
.nav-container {
    position: relative;
    z-index: 1000;
    /* Increased z-index */
}

.nav {
    z-index: 1;
}

.item-card {
    border: 1px solid #ddd;
    border-radius: 5px;
    padding: 20px;
    margin-bottom: 20px;
}

.item-card img {
    max-width: 300px;
    max-height: 300px;
    height: auto;
}

.item-title {
    font-weight: bold;
}

.item-price {
    color: #ffffff;
}


.itemImage {
    max-height: 40dvh;
    max-width: auto;
    background-size: cover;
    background-position: center;
    border-radius: 20px;
    box-shadow: 0px 0px 20px #423826;
    border: solid thick #00000082;
    overflow: hidden;
    transition: transform ease-in-out 2s;
}

.itemImage:hover {
    box-shadow: 0px 0px 20px #2c2519;
    transform: scale(1.05);
}

.glassCard {
    background: rgba(15, 15, 15, 0.354);
    border-radius: 16px;
    box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(8.1px);
    -webkit-backdrop-filter: blur(8.1px);
    border: 1px solid rgba(15, 15, 15, 0.26);
}

.purchase-btn {
    position: absolute;
    bottom: -19px;
    /* left: 76px; */
}

.bground-img {
    background-image: url(src/assets/img/WhiteParchment.png);
    background-position: center;
    background-size: cover;
    box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
}
</style>