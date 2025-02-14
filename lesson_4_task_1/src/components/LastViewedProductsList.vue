<template>
    <div>
        <div>
            <h2>Останні переглянуті товари</h2>
            <div class="product-list">
                <product-card 
 v-for="product in products"
:key="product.id"
:productImg="product.img"
:productTitle="product.title"
:addReview="product.review"
:productAvailability="product.availability"
:productPrice="product.price"
/>
            </div>     
    </div>
    </div>
</template>

<script>
import ProductCard from "./ProductCard.vue"
    export default {
        name: "LastViewProductsList",
        components: {
            ProductCard,
        },
        data() {
            return {
                 products: [
        { id: 1, img: './images/phones/ASSET_MMS_142867016.webp', title: 'Портативний екран TouYinger 130', review: "Залишити відгук ", availability: "Є в наявності", price: 1899 },
          { id: 2, img: './images/products/ASSET_MMS_115102352.webp', title: 'Портативний екран TouYinger 130', review: "Залишити відгук ", availability: "Є в наявності", price: 1899 },
          { id: 3, img: './images/phones/ASSET_MMS_142867016.webp', title: 'Портативний екран TouYinger 130', review: "Залишити відгук ", availability: "Є в наявності", price: 1899 },
        
      ]
            }
        },
    }
</script>

<style lang="css" scoped>
.product-list{
    display: inline-grid;
    grid-template-columns: 1fr 1fr 1fr;
}

</style>