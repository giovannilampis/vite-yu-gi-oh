<script>
export default {
    name: 'FoundCardsNumber',
    props: ['cardsNumber']
}

</script>

<template>
    <div class="container-found-cards">
        <h4>Numero dei personaggi trovati: {{ cardsNumber }} </h4>
    </div>
</template>

<style lang="scss" scoped>

    .container-found-cards {
        width: 80%;
        margin: 0 auto;
        background-color: rgba(33, 37, 41, 1);
        color: white;
        height: 4rem;
    }

    h4 {
        line-height: 4rem;
        padding-left: 3rem;
    }

</style>