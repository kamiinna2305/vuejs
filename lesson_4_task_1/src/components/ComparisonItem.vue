<template>

<img class="image__card" :src="imageSrc" :alt="altText">
    
</template>

<script>
    export default {
        name: "ComparisonItem",
           props: {
            imageSrc: {
                type: String,
                required: true 
            },
            altText: {
                type: String,
                required:true
            }
        },
    }
</script>

<style lang="css" scoped>

.image__card{
max-width: 200px;

}
</style>