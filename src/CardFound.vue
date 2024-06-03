<script>
import { store } from "./store.js";
export default {
    name:'CardFound',
    data(){
        return {
            store,
        }
    }
}
</script>
<template>
    <div>{{ store.results.length }} risultati trovati</div>
</template>