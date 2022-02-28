<template>




<Header/>
<Main/>
<Footer/>


</template>

<script>

    
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    Main,Footer,Header
  }
}
</script>

<style>
/* @import "./components/css/flex.scss"; */



</style>
