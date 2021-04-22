<template>
    <header>
        <h1>{{ title }}</h1>
        <Button v-show="homePage"
            :text="showAddRecord ? 'Close' : 'Add New Weight'" 
            @button-click="$emit('toggle-add-record')" 
            :color="showAddRecord ? 'red' : 'green'"/>
    </header>
</template>

<script>
import Button from './Button'

export default {
    name: 'Header',
    props: {
        title: String,
        showAddRecord: Boolean
    },
    components: {
        Button
    },
    computed: {
        homePage() {
            if(this.$route.path === '/'){
                return true
            }else{
                return false
            }
        }
    }
}
</script>

<style scoped>
h1{
    font-family: 'Mukta', sans-serif;
    margin: 0px;
    text-transform: uppercase;
}
header{
    display: grid;
    grid-template-columns: auto 130px;
}
</style>