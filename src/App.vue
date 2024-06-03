<script>
import CardFound from './CardFound.vue';
import CardList from './CardList.vue';
import { store } from './store.js'


export default {
  components: {
    CardFound,
    CardList,
  },
  data(){
    return {
      store,
      cards: []
    },
  },
  methods:{
    cardsGen() {
      axios.get("https://rickandmortyapi.com/api/character")
                    .then(response => {
                        this.cards.push(response.data)
                    })
      }
    }
  created(){
    axios.get(this.store.apiUrl).then((response) => {
      this.store.results = response.data.results
      this.store.info = response.data.info
    })
  }
}
</script>

<template>
  <CardFound></CardFound>
  <CardList></CardList>
</template>

<style scoped>
</style>
