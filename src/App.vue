<script >
import axios from 'axios';
import {store} from './store'
import HeaderComp from '../src/assets/components/HeaderComp.vue'
import FoundCardsNumber from '../src/assets/components/FoundCardsNumber.vue'
import CardsCollection from '../src/assets/components/CardsCollection.vue'
import FindCard from '../src/assets/components/FindCard.vue'
import SelectArchetype from '../src/assets/components/SelectArchetype.vue'



export default{
  name: 'app',
  components: {
    HeaderComp,
    FindCard,
    SelectArchetype,
    FoundCardsNumber,
    CardsCollection
  },
  data() {
    return{
      store
    }
  },
  computed: {



  },
  created() {
    this.callApi()
  },
  methods: {
    callApi(){

      if( this.store.textSearch !== '' ){

                  // modify callApi method
          axios.get(`https://db.ygoprodeck.com/api/v7/cardinfo.php?name=${this.store.textSearch}`).then( (response) =>{

          const apiData = response.data.data;

          console.log(response.data.data);

          this.store.arrayCards = apiData;

          this.store.textSearch = ''

          } )

      } else{

          axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0').then( (response) =>{
      
          const apiData = response.data.data;

          console.log(response.data.data)

          this.store.arrayCards = apiData;

          })

      }
    
    }
  },
}

</script>

<template>

  <HeaderComp :titleProps="'Yu-Gi-Oh API project'"/> 

  <main>

    <FindCard  @nameEmit="callApi"/>

    <SelectArchetype/>

    <FoundCardsNumber :cardsNumber="store.arrayCards.length"/>

    <CardsCollection/> 

  </main>


</template>

<style lang="scss">

    @use './style/main.scss';

    main {
      background-color: rgba(212, 143, 56, 1);
      padding: 4rem 6rem;
    }

</style>
