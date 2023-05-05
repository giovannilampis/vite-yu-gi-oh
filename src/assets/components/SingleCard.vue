<script>
export default {
    name: 'SingleCard',
    props: ['cardDetails']
}

</script>

<template>
    <div class="my-card">

        <img :src="cardDetails.card_images[0].image_url_small" :alt="cardDetails.name">
        <h5>{{ cardDetails.name }}</h5>
        <h6>{{ cardDetails.archetype }}</h6>
        
    </div>
</template>

<style lang="scss" scoped>

</style>