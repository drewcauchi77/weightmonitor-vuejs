<template>
    <AddRecord v-show="showAddRecord"/>
    <Records :records="records"/>
</template>

<script>
import AddRecord from '../components/AddRecord'
import Records from '../components/Records'

export default {
    name: 'Home',
    components: {
        AddRecord,
        Records
    },
    props: {
        showAddRecord: Boolean
    },
    data() {
        return {
            records: []
        }
    },
    created() {
        this.records = [
            {
                id: 1,
                date: "19/04/2021",
                weight: 68,
                height: 172,
                bmi: 22.99,
            },
            {
                id: 2,
                date: "20/04/2021",
                weight: 69,
                height: 172,
                bmi: 23.32,
            },
            {
                id: 3,
                date: "21/04/2021",
                weight: 67,
                height: 173,
                bmi: 22.39,
            }
        ]
    }
}
</script>