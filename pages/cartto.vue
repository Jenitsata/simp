<template>
  <div class="checkout-box">
    <ul class="checkout-list">
      <transition-group name="fade">
        <li
          v-for="(product, index) in products"
          :key="index"
          class="checkout-product"
        >
          <h3 class="product-name">{{ product.name }}</h3>
          <span class="product-price">฿ {{ product.price }} </span>
        </li>
      </transition-group>
    </ul>
    
    <h3 class="total">Total: ฿ {{ total }}</h3>
  </div>
</template>

<script>
export default {
    
};
</script>

<style>
.checkout-box {
  width: 100%;
  max-width: 900px;
  display: flex;
  flex-direction: column;
  margin: 50px auto;
  box-sizing: border-box;
  padding: 1em;
}
 .checkout-list {
    padding: 0;
  }
  .checkout-product {
    display: grid;
    grid-template-columns: 1fr 3fr 2fr .5fr;
    background-color: #fff;
    box-shadow: 0px 0px 10px rgba(73, 74, 78, 0.1);
    border-radius: 5px;
    list-style: none;
    box-sizing: border-box;
    padding: .8em;
    margin: 1em 0;
  }
  .product-name {
    box-sizing: border-box;
  }
  .product-price {
    font-size: 1.2em;
    font-weight: bold;
  }
    .total {
    font-size: 2em;
    font-weight: bold;
    align-self: flex-end;
  }

</style>
