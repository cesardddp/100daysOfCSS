<template>
  <Header />

  <main class>
    <Main />
    <br />
    <hr />
    <br />
    <CardFlex />
  </main>

  <Footer />
</template>

<script>


import Main from './components/NavFlex.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'
import CardFlex from './components/CardsFlex.vue'



export default {
  name: 'App',
  components: {
    Main, Footer, Header, CardFlex
  }
}
</script>

<style>
/* @import "./components/css/flex.scss"; */
@import url("https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;500;700&display=swap");

#app {
  width: 80%;
  font-family: "Roboto",monospace, sans-serif;
  font-weight: 500;
}
</style>
