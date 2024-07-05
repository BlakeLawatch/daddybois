<template>
    <div class="nav-container col-md-12">
        <Navbar />
    </div>
    <main class="container-fluid background-image top-page">
        <section class="row justify-content-center">

            <button class="filter-buttons text-uppercase" @click="changeFilter('')">All</button>
            <button class="filter-buttons text-uppercase" @click="changeFilter(merchType)"
                v-for="merchType in merchTypes" :key="merchType">{{ merchType
                }}</button>


        </section>

        <section class="row p-5 justify-content-center">

            <!-- <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BrownMug.png" alt="">
                <FORM action="https://www.paypal.com/cgi-bin/webscr" method="post">
                    <input type="hidden" name="cmd" value="_s-xclick">
                    
                </FORM>
            </div> -->
            <form action="https://www.paypal.com/cgi-bin/webscr" method="post" target="_top">
                <input type="hidden" name="cmd" value="_s-xclick" />
                <input type="hidden" name="hosted_button_id" value="NYL23AU9VCWQ2" />
                <input type="hidden" name="currency_code" value="USD" />
                <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif" border="0"
                    name="submit" title="PayPal - The safer, easier way to pay online!" alt="Buy Now" />
                <p class="description-btn text-center glassCard p-2 text-light">16 oz Brown Mug <br> $12.95 </p>
            </form>

            <div id="mugs" class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueDarkblueMug.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">16 oz Light Blue Mug <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMug.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">16 oz Dark Blue Mug <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 mugs position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ClearMug.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">12 oz Glass Mug <br> $12.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GreyOrangeMug.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">16 oz Grey/Orange Mug
                    <br> $12.95
                </p>
            </div>
            <!-- 
             t-shirts 23.95
             beanie 18.95
             hats 25.95 -->

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/CornerMug.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Goldys Corner 12 oz Mug
                    <br> $12.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GroundCoffeeBeans.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Dawson Taylor Ground
                    Coffee <br> $15.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WholeCoffeeBeans.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Dawson Taylor Whole
                    Coffee Beans <br> $15.95
                </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Beanie.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Black Beanie <br> $18.95 </p>
            </div>


            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayWomansShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Gray Woman's Shirt <br> $23.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PinkWomansShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Pink Woman's Shirt <br> $23.95 </p>
            </div>


            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/PurpleWomansShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Purple Woman's Shirt <br> $23.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GrayMensShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Gray Men's Shirt <br> $23.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/BlueMensShirt.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Blue Men's Shirt <br> $23.95 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Chapstick.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Goldys Chap Stick <br> $2.00 </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GiftCard.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Gift Card <br> <i>works at restaurant
                        and
                        corner</i> </p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/ChampagneGlass.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/WaterBottle.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/Tumbler.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GoldysSpice.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Goldys Spice Mix <br> $12.95</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/GreenThermos.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <img class="itemImage" src="src/assets/img/ShopImages/OrangeThermos.png" alt="">
                <p class="glassCard text-light p-2 text-center description-btn">Add To Cart</p>
            </div>

            <div class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <div class="col-8 itemImage blue-hat"></div>
                <p class="glassCard text-light p-2 text-center description-btn">Blue Trucker Hat <br> $25.95</p>
            </div>

            <div id="hats" class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <div class="col-8 itemImage gray-hat"></div>
                <p class="glassCard text-light p-2 text-center description-btn">Gray Trucker Hat <br>
                    $25.95</p>
            </div>

            <div id="hats" class="col-md-3 col-10 position-relative d-flex justify-content-center my-4">
                <div class="col-8 itemImage dad-hat"></div>
                <p class="glassCard text-light p-2 text-center description-btn">Yellow Dad Hat <br> $25.95 </p>
            </div>

        </section>
    </main>
    <Bottom />

</template>


<script>
import { hide } from '@popperjs/core';
import { ref } from 'vue';




export default {
    setup() {
        const merchTypes = ['mugs', 'shirts', 'cups', 'hats', 'misc']
        const filteredMerch = ref('')
        return {
            merchTypes,
            changeFilter(merch) {
                // filteredMerch.value = merch
                let shop = document.getElementsByName(merch)
                if (filteredMerch.value) {
                    return shop
                }
                else hide



            }

        }
    }
}


</script>


<style lang="scss" scoped>
.itemImage {
    height: 40dvh;
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

.description-btn {
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

.blue-hat {
    background-image: url(src/assets/img/ShopImages/BlueTruckerHat1.png);
}

.blue-hat:hover {
    background-image: url(src/assets/img/ShopImages/BlueTruckerHat2.png);
    transition: ease-in-out 1s;
}

.gray-hat {
    background-image: url(src/assets/img/ShopImages/GrayTruckerHat1.png);
}

.gray-hat:hover {
    background-image: url(src/assets/img/ShopImages/GrayTruckerHat2.png);
    transition: ease-in-out 1s;
}

.dad-hat {
    background-image: url(src/assets/img/ShopImages/DadHat1.png)
}

.dad-hat:hover {
    background-image: url(src/assets/img/ShopImages/DadHat2.png);
    transition: ease-in-out 1s;
}

.filter-buttons {
    height: 6dvh;
    width: 9dvw;
    border-radius: 30px;
    background-color: var(--bs-info);
    color: var(--bs-danger);
    font-weight: 600;
    border: .15rem solid var(--bs-danger);
    margin-left: .5rem;
    margin-right: .5rem;
}

@media (max-width: 767px) {
    .filter-buttons {
        height: 6dvh;
        width: 20dvw;
        margin-top: 1rem;
        margin-left: 1rem;
        margin-right: 1rem;
    }

}

.filter-buttons:hover {
    background-color: var(--bs-danger);
    color: var(--bs-info);
    text-shadow: 1px 1px 2px var(--bs-info);
    transition: ease-in-out .3s;
}
</style>