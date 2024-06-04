<template>
  <div>
    <div id="paypal-button-container"></div>
  </div>
</template>

<script>
export default {
  name: 'PayPalButton',
  mounted() {
    const script = document.createElement('script');
    script.src = `https://www.paypal.com/sdk/js?client-id=YOUR_CLIENT_ID&currency=USD`;
    script.addEventListener('load', this.initPayPalButton);
    document.body.appendChild(script);
  },
  methods: {
    initPayPalButton() {
      paypal.Buttons({
        createOrder: (data, actions) => {
          return actions.order.create({
            purchase_units: [{
              amount: {
                value: '0.01' // Replace with the actual amount
              }
            }]
          });
        },
        onApprove: (data, actions) => {
          return actions.order.capture().then(details => {
            alert('Transaction completed by ' + details.payer.name.given_name);
          });
        }
      }).render('#paypal-button-container');
    }
  }
}
</script>

<style scoped>
/* Add any styles you need for your component here */
</style>
