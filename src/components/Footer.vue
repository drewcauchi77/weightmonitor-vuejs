<template>
    <footer>
        <p>Andrew 2021</p>
        <router-link to="/about">About</router-link>
    </footer>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style scoped>
footer{
    display: grid;
    grid-template-columns: repeat(2, 100px);
    margin: 0 auto;
    width: fit-content;
    padding-top: 30px;
    grid-column-gap: 30px;
    font-family: 'Mukta', sans-serif;
}
p{
    margin: 0px;
    text-align: center;
}
a{
    color:black;
    text-align: center;
}
</style>