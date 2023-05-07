<script>
import { store } from '../../store';

import SingleCard from './SingleCard.vue';

export default {
    name: 'CardsCollection',
    components: {
        SingleCard
    },
    data(){
        return{
            store
        }
    }
}
</script>

<template>

    <section>

        <div class="container-white">

            <div class="cards-container row">

                <SingleCard 
                v-for="(element, index) in store.arrayCards" 
                :key="index"
                :cardDetails="element"/>

            </div>

        </div>

    </section>

</template>

<style lang="scss" scoped>

    * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
    .container-white {
        width: 80%;
        background-color: white;
        margin: 0 auto;
    }

    .cards-container {
        width: 95%;
        margin: 0 auto;
    }

</style>