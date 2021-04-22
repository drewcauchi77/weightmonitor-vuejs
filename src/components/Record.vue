<template>
    <div class="single-record">
        <h3>{{ record.date }}</h3>
        <div class="record-details">
            <span>Weight: {{ record.weight }}kg</span>
            <span>Height: {{ record.height }}cm</span>
        </div>
        <span class="bmi-details">BMI: {{ record.bmi }}</span>
    </div>
</template>

<script>
export default {
    name: 'Record',
    props: {
        record: Object
    }
}
</script>

<style scoped>
.single-record{
    padding: 20px 20px;
    margin: 5px 0px;
    font-family: 'Mukta', sans-serif;
    cursor: default;
    display: grid;
    grid-template-columns: repeat(3, auto);
    border: 1px solid black;
}
span{
    display: block;
    align-self: center;
}
.bmi-details{
    font-size: 18px;
    font-weight: 700;
}
h3{
    margin: 0px;
    align-self: center;
}
</style>