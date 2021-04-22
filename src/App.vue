<template>
  <div class="container">
    <Header title="Weight Monitor" @toggle-add-record="toggleAddRecord" :showAddRecord="showAddRecord"/>
    <router-view :showAddRecord="showAddRecord"></router-view>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header'
import Footer from './components/Footer'

export default {
    name: 'App',
    components: {
        Header,
        Footer
    },
    data() {
        return {
            showAddRecord: false
        }
    },
    methods: {
        toggleAddRecord() {
            this.showAddRecord = !this.showAddRecord
        }
    }
}

// API
// Ordering array by date
// form to api post

</script>

<style scoped>
.container{
    width: 400px;
    border: 2px solid grey;
    border-radius: 20px;
    padding: 30px;
    margin: 0 auto
}
</style>