<template>
    <div>
<div class="product">
    <img src="/images/icons/favorite.webp" alt="" class="favorites">
    <img :src="productImg" alt="" class="image">
    <p class="product-title">{{productTitle}}</p>
    <div>Залишити відгук</div>
    <div>{{productAvailability}}</div>
    <div>{{productPrice}} гривень</div>
</div>
    </div>
</template>

<script>
    export default {
        name: "ProductCard",
        props: {
            productImg: {
                type: String,
                required: true
            },
            productTitle: {
                type: String,
                required: true
            },
            addReview: {
                type: String,
                required: true
            },
            productAvailability: {
                type: String,
                required: true
            },
            productPrice: {
                type: Number,
                required: true
            }

        },
    }
</script>

<style lang="css" scoped>
.product{
    position: relative;
    display: flex;
    flex-direction: column;
    max-width: 300px;
    padding: 10px;
    border: 1px solid grey;
    padding-top: 40px;
}
.favorites{
    width: 36px;
    position: absolute;
    top: 10px;
    right: 10px;
}

.image{
   max-width: 200px;
   height: auto;
   align-items: center;
}

.product-title{
    font-size: 18px;
    display: flex;
    flex-wrap: wrap;
}

</style>