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
    <div>
        <SingleCard 
            v-for="(element, index) in store.arrayCards" 
            :key="index"
            :cardDetails="element"/>
    </div>
</template>

<style lang="scss" scoped>

</style>