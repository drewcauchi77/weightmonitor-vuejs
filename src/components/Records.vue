<template>
    <div class="records">
        <div class="record" v-for="record in records" :key="record.id">
            <Record :record="record"/>
        </div>
    </div>
</template>

<script>
import Record from './Record'

export default {
    name: 'Records',
    props: {
        records: Array
    },
    components: {
        Record
    }
}
</script>