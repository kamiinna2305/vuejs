<template>
  <comparison-lists/>
  <last-view-products-list/>
  
</template>

<script>
import ComparisonLists from './components/ComparisonLists.vue';
import LastViewProductsList from './components/LastViewedProductsList.vue'

export default {
  name: 'App',
  components: {
    ComparisonLists,
    LastViewProductsList,
  }
}
</script>

<style>

</style>
