<script >

import HeaderComp from '../src/assets/components/HeaderComp.vue'
import CardsCollection from '../src/assets/components/CardsCollection.vue'

import axios from 'axios';

export default{
  name: 'app',
  components: {
    HeaderComp,
    CardsCollection
  },
  created() {
    axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=3')
    .then(response =>{
      this.carte = response.data.data;
    })
},
}


</script>

<template>
<HeaderComp :titleProps="'ci'+'anso'"/>  

  <main>
    <CardsCollection /> 
  </main>


</template>

<style lang="scss">
@use './style/main.scss';
</style>
