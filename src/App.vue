<script>
import CardFound from './CardFound.vue';
import CardList from './CardList.vue';
import HeaderList from './HeaderList.vue';
import { store } from './store.js'

import axios from 'axios';
export default {
  components: {
    CardFound,
    CardList,
    HeaderList
  },
  data(){
    return {
      store,
      cards: []
    }
  },
  methods:{
    cardsGen() {
      axios.get("https://rickandmortyapi.com/api/character")
                    .then(response => {
                        this.cards.push(response.data)
                    })
      }
    },
  created(){
    axios.get(this.store.apiUrl).then((response) => {
      this.store.results = response.data.results
      this.store.info = response.data.info
    })
  }
}
</script>

<template>
  <HeaderList></HeaderList>
  <CardList></CardList>
  <CardFound></CardFound>
</template>

<style scoped>
</style>
