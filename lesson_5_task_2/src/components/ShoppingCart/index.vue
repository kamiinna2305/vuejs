<template>
    <div>
<h2 class="cart-title">Кошик</h2>

      <div 
      v-for="item in cart" 
      :key="item.id"
      >
        <product-item/>
      </div>
    
    </div>
</template>

<script>
import ProductItem from '../ListProducts/ProductItem.vue';
    export default {
        name: "ShoppingCart",
        components: {
            ProductItem,
        },
        props: {
            cart: {
                type: Array,
                required: true 
            },
        },
    }
</script>

<style  scoped>
.cart-title{
    color: #05c26d;;
}
</style>