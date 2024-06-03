<script>
import { store } from "./store.js";
export default {
    name:'CardList',
    data(){
        return {
            store
        }
    }
}
</script>

<template>
    <div class="container mt-5">
        <ul class="row">
            <li class="col-3" v-for="card in store.results">
                <img :src="card.image">
                <h2>{{ card.name }}</h2>
                <p>{{ card.status }}</p>
                <p>{{ card.species }}</p>
            </li>
        </ul>
    </div>
</template>
<style scoped>
    img{
        width: 100%;
    }
    
</style>
