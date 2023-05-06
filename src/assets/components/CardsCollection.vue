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

                <SingleCard 
                    v-for="(element, index) in store.arrayCards" 
                    :key="index"
                    :cardDetails="element"/>

            </div>
        </div>

    </section>

</template>

<style lang="scss" scoped>

    section {
        background-color: rgba(212, 143, 56, 1);
        padding: 5rem 0;
    }

    .container {
        width: 80%;
    }

    .container-white {
        background-color: white;
        padding: 5rem;
    }

</style>