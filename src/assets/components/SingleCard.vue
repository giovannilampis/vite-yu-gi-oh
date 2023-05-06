<script>
export default {
    name: 'SingleCard',
    props: ['cardDetails']
}

</script>

<template>

    <div class="my-card d-flex flex-column justify-content-center align-items-center mx-4 col-12 col-md-4 col-lg-2">

        <img :src="cardDetails.card_images[0].image_url_small" :alt="cardDetails.name">
        <p><b class="text-white">{{ cardDetails.name }}</b></p>
        <h6>{{ cardDetails.archetype }}</h6>

    </div>
 
</template>

<style lang="scss" scoped>

    * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        img {
            margin: 0 auto;
        }
    .my-card {
        background-color: rgba(212, 143, 56, 1);
        margin-bottom: 1rem;
    }

</style>