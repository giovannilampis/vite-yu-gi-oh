<script>
export default {
    name: 'SingleCard',
    props: ['cardDetails']
}

</script>

<template>

    <div class="my-card mx-3 col-12 col-md-4 col-lg-2">

        <img class="mb-2" :src="cardDetails.card_images[0].image_url_small" :alt="cardDetails.name">
        <h6 class="text-white">{{ cardDetails.name }}</h6>
        <small>{{ cardDetails.archetype }}</small>

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
            max-width: 80%;
        }
    .my-card {
        background-color: rgba(212, 143, 56, 1);
        margin-bottom: 1rem;
        text-align: center;
        padding: 0.5rem;
        display: flex;
        flex-direction: column;
        justify-content: stretch;
    }

    small {
        align-items: flex-end;
    }

</style>