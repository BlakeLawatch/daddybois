<template>
  <div class="nav-container col-md-12">
    <Navbar />
  </div>
  <main class="container-fluid background-image top-page">
    <section class="row justify-content-center">
      <button class="filter-buttons text-uppercase" @click="changeFilter('')">All</button>
      <button class="filter-buttons text-uppercase" @click="changeFilter(merchType)" v-for="merchType in merchTypes"
        :key="merchType">
        {{ merchType }}
      </button>
    </section>

    <section class="row p-5 justify-content-center">
      <div v-for="item in filteredMerch" :key="item.id" class="col-md-3 col-10 position-relative text-center my-4">
        <div class="d-flex justify-content-center pb-5">
          <!-- <div v-if="item.class"></div> -->
          <img class="itemImage" :src="item.image">
          <p class="description-btn text-center glassCard p-2 text-light">{{ item.description }} <br> {{ item.price }}
          </p>
        </div>
        <div class="d-flex justify-content-center" v-if="item.paypalButtonId">
          <form :action="'https://www.paypal.com/cgi-bin/webscr'" method="post" target="_blank">
            <input type="hidden" name="cmd" value="_s-xclick" />
            <input type="hidden" name="hosted_button_id" :value="item.paypalButtonId" />
            <table class="text-center" v-if="item.size">
              <tr>
                <td>
                  <input type="hidden" name="on0" :value="item.size" />
                  Size
                </td>
              </tr>
              <tr>
                <td>
                  <select name="os0">
                    <option value="Small">
                      Small
                    </option>
                    <option value="Medium">
                      Medium
                    </option>
                    <option value="Large">
                      Large
                    </option>
                    <option value="X-Large">
                      X-Large
                    </option>
                  </select>
                </td>
              </tr>
            </table>
            <input type="hidden" name="currency_code" value="USD" />
            <input type="image" src="https://www.paypalobjects.com/en_US/i/btn/btn_buynow_LG.gif" border="0"
              name="submit" title="PayPal - The safer, easier way to pay online!" alt="Buy Now" />
          </form>
        </div>
      </div>
    </section>
  </main>
  <Bottom />
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const merchTypes = ['mugs', 'shirts', 'coffee', 'hats', 'misc'];
    const merchItems = ref([
      { id: 1, type: 'mugs', image: 'src/assets/img/ShopImages/BrownMug.png', description: '16 oz Brown Mug', price: '$12.95', paypalButtonId: 'NYL23AU9VCWQ2' },
      { id: 2, type: 'mugs', image: 'src/assets/img/ShopImages/BlueDarkblueMug.png', description: '16 oz Light Blue Mug', price: '$12.95', paypalButtonId: 'HTU5ZW7H9G64U' },
      { id: 3, type: 'mugs', image: 'src/assets/img/ShopImages/BlueMug.png', description: '16 oz Dark Blue Mug', price: '$12.95', paypalButtonId: 'UQNBC7PT47WYS' },
      { id: 4, type: 'mugs', image: 'src/assets/img/ShopImages/ClearMug.png', description: '12 oz Glass Mug', price: '$12.95', paypalButtonId: 'WURX3BPSWJJC4' },
      { id: 5, type: 'mugs', image: 'src/assets/img/ShopImages/GreyOrangeMug.png', description: '16 oz Grey/Orange Mug', price: '$12.95', paypalButtonId: 'BLX9W78Q85NWS' },
      { id: 6, type: 'mugs', image: 'src/assets/img/ShopImages/CornerMug.png', description: 'Goldys Corner 12 oz Mug', price: '$12.95', paypalButtonId: 'XLSA6UX2KH832' },
      { id: 7, type: 'coffee', image: 'src/assets/img/ShopImages/GroundCoffeeBeans.png', description: 'Dawson Taylor Ground Coffee', price: '$15.95', paypalButtonId: 'TJ63CA4FWK54Q' },
      { id: 8, type: 'coffee', image: 'src/assets/img/ShopImages/WholeCoffeeBeans.png', description: 'Dawson Taylor Whole Coffee Beans', price: '$15.95', paypalButtonId: '5VTDUAGXCCW8G' },
      { id: 9, type: 'hats', image: 'src/assets/img/ShopImages/Beanie.png', description: 'Black Beanie', price: '$18.95', paypalButtonId: 'LJJ4E24V9Y7XQ' },
      // { id: 10, type: 'misc', image: 'src/assets/img/ShopImages/Chapstick.png', description: 'Goldys Chap Stick', price: '$2.00', paypalButtonId: 'JR37TTV8MXRBU' },
      { id: 10, type: 'misc', image: 'src/assets/img/ShopImages/GiftCard.png', description: 'Gift Card, works at restaurant and corner', price: '$2.00', paypalButtonId: 'KKWVD7WUR2RRL' },
      { id: 11, type: 'misc', image: 'src/assets/img/ShopImages/ChampagneGlass.png', description: 'Champagne Glass', price: '$10.95', paypalButtonId: 'RUYB6NBTEL77E' },
      { id: 12, type: 'misc', image: 'src/assets/img/ShopImages/WaterBottle.png', description: 'Water Bottle', price: '$14.95', paypalButtonId: 'P2UZJGLLXLD88' },
      { id: 13, type: 'misc', image: 'src/assets/img/ShopImages/Tumbler.png', description: 'Tumbler', price: '12.95', paypalButtonId: 'EKAQYT99LPJCC' },
      { id: 14, type: 'misc', image: 'src/assets/img/ShopImages/GoldysSpice.png', description: 'Goldys Spice Mix', price: '$12.95', paypalButtonId: '9KMJJ33MBQ87A' },
      { id: 15, type: 'misc', image: 'src/assets/img/ShopImages/GreenThermos.png', description: 'Green Thermos', price: '$16.95', paypalButtonId: '7QWGY7NKFF3CA' },
      { id: 16, type: 'misc', image: 'src/assets/img/ShopImages/OrangeThermos.png', description: 'Orange Thermos', price: '$16.95', paypalButtonId: '29CM3AUGAJ56J' },
      { id: 17, type: 'hats', image: 'src/assets/img/ShopImages/BlueTruckerHat1.png', description: 'Blue Trucker Hat', price: '$25.95', paypalButtonId: 'AG5UKR4WFEDUA' },
      { id: 18, type: 'hats', image: 'src/assets/img/ShopImages/GrayTruckerHat1.png', description: 'Gray Trucker Hat', price: '$25.95', paypalButtonId: 'SH47SZ86B7X22' },
      { id: 19, type: 'hats', image: 'src/assets/img/ShopImages/DadHat1.png', description: 'Yellow Dad Hat', price: '$25.95', paypalButtonId: '8AJ4LRC47B3XW' },
      { id: 20, type: 'shirts', image: 'src/assets/img/ShopImages/GrayWomansShirt.png', description: 'Gray Woman\'s Shirt', price: '$23.95', paypalButtonId: '8ZJTRRMD9NRRE', size: 's' },
      { id: 21, type: 'shirts', image: 'src/assets/img/ShopImages/PinkWomansShirt.png', description: 'Pink Woman\'s Shirt', price: '$23.95', paypalButtonId: '64ADW4AD65ZNN', size: 's' },
      { id: 22, type: 'shirts', image: 'src/assets/img/ShopImages/PurpleWomansShirt.png', description: 'Purple Woman\'s Shirt', price: '$23.95', paypalButtonId: 'SUEZXHWCKV7QU', size: 's' },
      { id: 23, type: 'shirts', image: 'src/assets/img/ShopImages/GrayMensShirt.png', description: 'Gray Men\'s Shirt', price: '$23.95', paypalButtonId: 'H6X469CYDMU4G', size: 's' },
      { id: 24, type: 'shirts', image: 'src/assets/img/ShopImages/BlueMensShirt.png', description: 'Blue Men\'s Shirt', price: '$23.95', paypalButtonId: 'ZJEFZGRS4REU8', size: 's' },
    ]);
    const filteredMerch = ref(merchItems.value);

    const changeFilter = (filter) => {
      if (filter === '') {
        filteredMerch.value = merchItems.value;
      } else {
        filteredMerch.value = merchItems.value.filter(item => item.type === filter);
      }
    };

    return {
      merchTypes,
      filteredMerch,
      changeFilter
    };
  }
};
</script>

<style lang="scss" scoped>
// .itemImage {
//   height: 40dvh;
//   max-width: auto;
//   background-size: cover;
//   background-position: center;
//   border-radius: 20px;
//   box-shadow: 0px 0px 20px #423826;
//   border: solid thick #00000082;
//   overflow: hidden;
//   transition: transform ease-in-out 1s;
// }

// .itemImage:hover {
//   box-shadow: 0px 0px 20px #2c2519;
//   transform: scale(1.05);
// }

.glassCard {
  background: #0f0f0f5a;
  border-radius: 16px;
  box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(8.1px);
  -webkit-backdrop-filter: blur(8.1px);
  border: 1px solid rgba(15, 15, 15, 0.26);
}

.description-btn {
  position: absolute;
  bottom: 40px;
}

.bground-img {
  background-image: url(src/assets/img/WhiteParchment.png);
  background-position: center;
  background-size: cover;
  box-shadow: inset 0px 10px 10px rgb(93, 91, 91);
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

.itemImage {
  height: 40dvh;
  width: 100%;
  object-fit: cover;
  border-radius: 20px;
  box-shadow: 0px 0px 20px #423826;
  border: solid thick #00000082;
  overflow: hidden;
  transition: transform 0.3s ease-in-out;
}

.itemImage:hover {
  box-shadow: 0px 0px 20px #2c2519;
  transform: scale(1.05);
}
</style>