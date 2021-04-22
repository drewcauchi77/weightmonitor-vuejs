<template>
    <form @submit.prevent="onSubmit" class="add-form">
        <div class="form-control">
            <label>Date</label>
            <input type="date" v-model="date" name="date" />
        </div>

        <div class="form-control">
            <label>Weight(in kg)</label>
            <input type="number" v-model="weight" name="weight" placeholder="Insert weight in KG" />
        </div>

        <div class="form-control">
            <label>Height(in cm)</label>
            <input type="number" v-model="height" name="height" placeholder="Insert height in CM" />
        </div>

        <input type="submit" value="Save Record" />
    </form>
</template>

<script>
export default {
    name: 'AddRecord',
    data() {
        return {
            date: '',
            weight: '',
            height: ''
        }
    },
    methods: {
        onSubmit() {
            console.log('test')
        }
    }
}
</script>

<style scoped>
form{
    padding: 40px 0px;
}
.form-control{
    display: grid;
    grid-template-columns: 100px auto;
    margin-bottom: 10px;
    font-family: 'Mukta', sans-serif;
}
input, input::placeholder{
    font-family: 'Mukta', sans-serif;
}
input[type=submit]{
    width: 100%;
    height: 30px;
    background-color: black;
    outline: none;
    color: white;
    text-transform: uppercase;
    border: none;
}
</style>