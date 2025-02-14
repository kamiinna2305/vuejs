<template>
    <div>
<div class="comparison">
    <h1> Списки порівнянь</h1>
    <div class="comparison__container">
    <h2>Мобільні телефони</h2>
    <h3>Кількість товарів: 3</h3>
    <div class="comparison__section">
    
    <comparison-item
    v-for="phone in phones"
    :key="phone.id"
    :image-src="phone.imageSrc"
    :alt-text="phone.altText"
    class="image__card"/>
</div>
</div>
</div>
    </div>
</template>

<script>
import ComparisonItem from './ComparisonItem.vue'
    export default {
  components: { ComparisonItem },
        name: "ComparisonLists",
        data() {
            return {
                phones: [
        { id: 1, imageSrc: './images/phones/ASSET_MMS_142867016.webp', altText: 'Phone 1' },
        { id: 2, imageSrc: './images/phones/iphone.webp', altText: 'Phone 2' },
        { id: 3, imageSrc: './images/phones/Redmi_Note.webp', altText: 'Phone 3' }
      ]
            }
        },
     
    }
</script>

<style lang="css" scoped>

.comparison__container{
    border: 1px solid grey;
    padding: 20px;
    border-radius: 10px;
}

.comparison__section{
    display: flex;
    flex-wrap: wrap;
    gap: 5px;

}
</style>