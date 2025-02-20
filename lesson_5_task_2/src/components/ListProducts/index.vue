<template>
    <div class="wrapper">
<product-item
v-for="product in productsListData"
:key="product.id"
:notebooks="product"
/>
    </div>
</template>

<script>
import ProductItem from './ProductItem.vue'
    export default {
        name: "ListProducts",
  components: { ProductItem },
  props: {
    productsListData: {
        type: Array,
        default: () => []
    },
  },     
    }
</script>

<style  scoped>
.wrapper{
    width: 600px;
}

</style>