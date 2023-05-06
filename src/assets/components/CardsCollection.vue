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

        <div class="container">

            <div class="container-white row">

                <div class="found-cards">


                </div>

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

    section {
        background-color: rgba(212, 143, 56, 1);
        padding: 5rem 0;
    }

    .container {
        width: 80%;
    }

    .found-cards {
        background-color: rgba(33, 37, 41, 1);
        height: 3rem;
    }

    .container-white {
        background-color: white;
        padding: 2rem;
    }

</style>