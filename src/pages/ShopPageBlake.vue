<template>
    <div class="nav-container col-md-12">
        <Navbar />
    </div>
    <main class="container-fluid background-image top-page">
        <!-- <section class="row">
                <button onclick="getMugs()">Mugs</button>
            </section> -->

        <section class="row p-5 justify-content-center">

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BrownMug.png" alt="">
                <p class="purchase-btn text-center glassCard p-2 text-light">16 oz Brown Mug <br> $12.95 </p>
                <FORM action="https://www.paypal.com/cgi-bin/webscr" method="post">
                    <input type="hidden" name="cmd" value="_s-xclick">

                </FORM>
            </div>

            <div id="mugs" class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueDarkblueMug.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">16 oz Light Blue Mug <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMug.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">16 oz Dark Blue Mug <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 mugs position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ClearMug.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">12 oz Glass Mug <br> $12.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GreyOrangeMug.png" alt="">
                <p data-aos="fade-right" class="glassCard text-light p-2 text-center purchase-btn">16 oz Grey/Orange Mug
                    <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/CornerMug.png" alt="">
                <p data-aos="fade-up" class="glassCard text-light p-2 text-center purchase-btn">Goldys Corner 12 oz Mug
                    <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GroundCoffeeBeans.png" alt="">
                <p data-aos="fade-up" class="glassCard text-light p-2 text-center purchase-btn">Dawson Taylor Ground
                    Coffee <br> $15.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WholeCoffeeBeans.png" alt="">
                <p data-aos="fade-left" class="glassCard text-light p-2 text-center purchase-btn">Dawson Taylor Whole
                    Coffee Beans <br> $15.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Beanie.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Black Beanie <br> $ </p>
            </div>


            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayWomansShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Gray Womans Shirt <br> $ </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PinkWomansShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Pink Womans Shirt <br> $ </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Chapstick.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Goldys Chap Stick <br> $2.00 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GiftCard.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Gift Card <br> <i>works at restaurant and
                        corner</i> </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PurpleWomensShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayMensShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMensShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ChampagneGlass.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WaterBottle.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Tumbler.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GoldysSpice.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Goldys Spice Mix <br> $12.95</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GreenThermos.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/OrangeThermos.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueTruckerHat1.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/DadHat1.png" alt="">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayTruckerHat1.png" alt="">
                <p data-aos="fade up" class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
            </div>
        </section>
    </main>
    <Bottom />

</template>


<script>



export default {
    setup() {
        function getMugs() {
            let elem = document.getElementById("mugs")
            return elem
            // getMugs
        }
        return {
            getMugs
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
    transition: transform ease-in-out 1s;
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
    bottom: -40px;
    /* left: 76px; */
}

.bground-img {
    background-image: url(src/assets/img/WhiteParchment.png);
    background-position: center;
    background-size: cover;
    box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
}
</style>