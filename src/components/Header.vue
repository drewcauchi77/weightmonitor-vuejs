<template>
    <header>
        <h1>{{ title }}</h1>
        <button>Add New Weight</button>
    </header>
</template>

<script>
export default {
    name: 'Header',
    props: {
        title: String
    }
}
</script>

<style scoped>
h1{
    font-family: 'Mukta', sans-serif;
    margin: 0px;
    text-transform: uppercase;
}
</style>