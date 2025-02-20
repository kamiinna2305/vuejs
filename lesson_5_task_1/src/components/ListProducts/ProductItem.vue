<template>
    <div class="container-product">
        <img 
        :src="productData.imgSrc" 
        alt="raspberry" 
        class="img"/>
        <a 
        :href="productData.link" 
        class="link-title">
        {{productData.title}}
        </a>
    </div>
</template>

<script>
    export default {
        name: 'ProductItem',
        props: {
            productData: {
                type: Object,
                default: () => ({}),
            },
        },
    }
</script>

<style  scoped>
.container-product{
    padding: 10px;
    text-align: center;
    max-width: 200px;
    height: 200px;
    background-color: #fff;
    border: solid 1px black;
    border-radius: 10px;
    transition: 0.8s;
}

.container-product:hover{
    box-shadow: 10px 10px 10px grey;
}

.img{
    width: 200px;
    height: 170px;
    border-radius: 10px;
    border: solid 1px black;
}

.link-title{
    text-decoration: none;
    color: black;
    font-size: 20px;
    transition: 0.3s;
}

.link-title:hover{
opacity: 0.5;
}
</style>