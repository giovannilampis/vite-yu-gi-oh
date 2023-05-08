<script>

import {store} from '../../store'

export default {
    name: 'FindCard',
    data() {
        return {
            store
        }
    },
}

</script>

<template>

    <div>

        <input type="text" placeholder="Ricerca carta" 
        v-model="store.textSearch">

    </div>

</template>

<style lang="scss" scoped>


</style>