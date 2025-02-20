<template>
  <div class="wrapper">
    <list-products
    :list-products-data = "products"
    />
  </div>
</template>

<script>
import ListProducts from '@/components/ListProducts'
import {products} from '@/data/products.js'

export default {
  name: 'App',
  components: {
    ListProducts, 
  },
  data() {
    return {
    products
    }
  },
}
</script>

<style>
body{
  background-color: #e8e3e3;
}
</style>


