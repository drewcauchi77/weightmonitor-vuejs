<template>
    <AddRecord v-show="showAddRecord" @add-record="addRecord"/>
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
    methods: {
        async addRecord(record) {
            const res = await fetch('api/records', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(record)
            })

            const data = await res.json()
            
            this.records = [...this.records, data]
        },
        async fetchRecords() {
            const res = await fetch('api/records')
            const data = await res.json()
            
            return data
        },
        sortArrayByDateDesc(array, key) {
            return array.sort(
                function(a, b){
                    var x = a[key] 
                    var y = b[key]

                    var xDateArray = x.split("/")
                    var yDateArray = y.split("/")

                    x = xDateArray[1] + '/' + xDateArray[0] + '/' + xDateArray[2]
                    y = yDateArray[1] + '/' + yDateArray[0] + '/' + yDateArray[2]

                    x = Date.parse(x)
                    y = Date.parse(y)

                    return ((x > y) ? -1 : ((x < y) ? 1 : 0))
                }
            )
        }
    },
    async created() {
        let unsortedRecords = await this.fetchRecords()
        this.records = this.sortArrayByDateDesc(unsortedRecords, 'date')
    },
    updated() {
        this.records = this.sortArrayByDateDesc(this.records, 'date')
    }
}
</script>