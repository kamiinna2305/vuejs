<template>
    <div class="container">
        <div >
          <img :src="notebooks.imgSrc" alt="notebook" class="img">
        </div>
        <div class="description">
            <div class="title">{{ notebooks.title }}</div>
            <div class="discount">Ваша економія: <span class="red">{{ notebooks.discount }}</span></div>
            <div class="old-price">{{ notebooks.oldPrice }}</div>
            <div class="block-price">
              <div class="price red">{{ notebooks.price }} ₴</div>
              <button @click="addToCart" class="btn">Купити</button>
            </div>
        </div>
    </div>

</template>

<script>
    export default {
        name: "ProductItem",
        props: {
            notebooks: {
                type: Object,
                default: () => ({})
            },
        },
        methods: {
            addToCart(notebooks) {
                this.$emit('add-to-cart', notebooks)
            }
        },
    }
</script>

<style scoped>
.container{
    border-bottom: solid 1px grey;
    display: flex;
    padding: 25px;
    gap: 15px;
}
.description{
    width: 100%;
}

.img{
    max-width: 150px;
}

.title{
    color: rgb(39, 126, 224);
    font-size: 18px;
}

.discount{
    font-size: 10px;
}

.red{
    color: red;
}

.old-price{
    color: gray;
    font-size: 18px;
    text-decoration: line-through;
}

.block-price{
    display: flex;
    justify-content: space-between;
}

.price{
    font-size: 24px;
}

.btn{
    color: white;
    background-color: #05c26d;
    border: none;
    border-radius: 5px;
    padding: 5px 10px;
}

</style>