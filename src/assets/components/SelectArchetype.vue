<script>

export default {
    name: 'SelectArchetype',
    data() {
        return {
            archetypeOptions: [
                'Alien',
                'Noble Knight',
                'Melodious',
                'Archfiend'
            ]
        }
    },
}

</script>

<template>
    <div>

        <select name="" id="">

            <option selected value="">Scegli l'archetipo</option>
            <option v-for="(element, index) in archetypeOptions" :key="index" :value="element">{{ element }}</option>

        </select>
        
    </div>
</template>

<style lang="scss" scoped>


</style>