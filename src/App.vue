<template>
  <div class="container">
    <Header title="Weight Monitor"/>
    <router-view></router-view>
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
    }
}
</script>

<style scoped>
.container{
    width: 380px;
    border: 2px solid grey;
    border-radius: 20px;
    padding: 30px;
    margin: 0 auto
}
</style>