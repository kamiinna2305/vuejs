<template>
  <div class="container-shop">
    <list-products
  :products-list-data = "notebooksList"
  />
  <shopping-cart
  />
  </div>


</template>

<script>
import ListProducts from './components/ListProducts'
import ShoppingCart  from './components/ShoppingCart';
import {notebooksList} from '@/data/products.js'

export default {
  name: 'App',
  components: {
    ListProducts,
    ShoppingCart
  },
  data() {
    return {
      notebooksList,
    }
  },
}
</script>

<style>
body{
  padding-top: 25px;
  width: 1000px;
  margin: 0px auto;
}

</style>
