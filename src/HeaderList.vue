<script>
export default {
    name:'HeaderList',
    
}
</script>
<template>
    <h1>Rick and Morty App</h1>
    <form>
        <input type="text" placeholder="Search character">
        <select>
            <option value="option-1">Select status</option>
        </select>
        <button>Search</button>
        <button>Reset</button>
    </form>

</template>
<style scoped>
h1{
    text-align: center;
}
form{
    display: flex;
    justify-content: center;
    gap: 10px;
}
form input, select, button{
    border: 1px solid gray;
    border-radius: 5%;
}

</style>