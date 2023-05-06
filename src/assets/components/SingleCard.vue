<script>
export default {
    name: 'SingleCard',
    props: ['cardDetails']
}

</script>

<template>

    <div class="my-card col-12 col-md-6 col-lg-2">

        <img :src="cardDetails.card_images[0].image_url_small" :alt="cardDetails.name">
        <p><b>{{ cardDetails.name }}</b></p>
        <h6>{{ cardDetails.archetype }}</h6>

    </div>
 
</template>

<style lang="scss" scoped>

    .my-card {
        background-color: rgba(212, 143, 56, 1);

    }

</style>