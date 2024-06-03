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
    <div>{{ store.info.pages }} risultati trovati</div>
</template>