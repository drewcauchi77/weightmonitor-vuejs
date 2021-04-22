<template>
    <button :style="{background: color}" @click="onClick">{{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    methods: {
        onClick() {
            this.$emit('button-click')
        }
    }
}
</script>

<style scoped>
button{
    height: 50px;
    align-self: center;
    color: white;
    outline: none;
    background-color: green;
    border: 1px solid white;
    font-family: 'Mukta', sans-serif;
    text-transform: uppercase;
    cursor: pointer;
}
</style>