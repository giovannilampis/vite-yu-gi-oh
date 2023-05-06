<script >

import HeaderComp from '../src/assets/components/HeaderComp.vue'
import CardsCollection from '../src/assets/components/CardsCollection.vue'
import axios from 'axios';
import {store} from './store'

export default{
  name: 'app',
  components: {
    HeaderComp,
    CardsCollection
  },
  data() {
    return{
      store
    }
  },
  created() {
    this.callApi()
  },
  methods: {
    callApi(){
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=10&offset=3').then( (response) =>{
      
      const apiData = response.data.data;
      // console.log(response.data.data)
      this.store.arrayCards = apiData;
    })
    }
  },
}

</script>

<template>
<HeaderComp :titleProps="'Yu-Gi-Oh API project'"/>  

  <main>
    <CardsCollection /> 
  </main>


</template>

<style lang="scss">
@use './style/main.scss';
</style>
