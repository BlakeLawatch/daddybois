<template>
    <div class="nav-container col-md-12">
        <Navbar />
    </div>
    <main class="container-fluid background-image top-page">
        <section class="row">
            <button onclick="getMugs()">Mugs</button>
        </section>

        <section class="row p-5 justify-content-center">

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="purchase-btn text-center glassCard p-2 text-light">16 oz Brown Mug <br> $12.95 </p>
                <FORM action="https://www.paypal.com/cgi-bin/webscr" method="post">
                    <input type="hidden" name="cmd" value="_s-xclick">
                    <img class="itemImage" src="src/assets/img/ShopImages/BrownMug.png" alt="">

                </FORM>
            </div>

            <div id="mugs" class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/BlueDarkblueMug.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMug.png" alt="">
            </div>

            <div class="col-md-3 col-10 mugs position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/ClearMug.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GreyOrangeMug.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/CornerMug.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GroundCoffeeBeans.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/WholeCoffeeBeans.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/Beanie.png" alt="">
            </div>


            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GrayWomansShirt.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/PinkWomansShirt.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/Chapstick.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GiftCard.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/PurpleWomensShirt.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GrayMensShirt.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMensShirt.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/ChampagneGlass.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/WaterBottle.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/Tumbler.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GoldysSpice.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GreenThermos.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/OrangeThermos.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/BlueTruckerHat1.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/DadHat1.png" alt="">
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <p class="glassCard text-light p-2 text-center purchase-btn">Add To Cart</p>
                <img class="itemImage" src="src/assets/img/ShopImages/GrayTruckerHat1.png" alt="">
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
    bottom: -32px;
    /* left: 76px; */
}

.bground-img {
    background-image: url(src/assets/img/WhiteParchment.png);
    background-position: center;
    background-size: cover;
    box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
}
</style>