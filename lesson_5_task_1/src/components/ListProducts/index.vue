<template>
    <div class="container">
<product-item
v-for="product in listProductsData"
:key="product.id"
:product-data="product"
/>
    </div>
</template>

<script>
import ProductItem from '@/components/ListProducts/ProductItem.vue'
    export default {
        name: 'ListProducts',
        components: {
            ProductItem,
        },
      props: {
        listProductsData: {
            type: Array,
            default: () => []
        },
      },
        
    }
</script>

<style  scoped>
.container{
    display: flex;
    gap: 10px;
    padding: 25px;
}
</style>