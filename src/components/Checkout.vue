<template>
  <Card title="Checkout Items" key="checkout">
    <p v-for="(k, i) in this.shoppingList" :key="i">
      Item: {{items[Number(k)].msg}} for ${{items[Number(k)].price}}
    </p>
  </Card>
</template>
<script>
import { Card } from 'ant-design-vue';

export default {
  props: ['shoppingList'],
  components: {
    Card
  },
  data: () => ({
    items: [
      { msg: 'First Product', price: 9.99 },
      { msg: 'Second Product', price: 19.99 },
      { msg: 'Third Product', price: 15.00 },
      { msg: 'Fancy Shirt', price: 137.00 },
      { msg: 'More Fancy', price: 109.99 },
      { msg: 'Extreme', price: 3.00 },
      { msg: 'Super Shirt', price: 109.99 },
      { msg: 'Epic Shirt', price: 3.00 },
    ]
  })
}
</script>
