<template>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <meta name="description" content="">
    <meta name="author" content="cesardddp@hotmail.com">

    <meta name="og:title" content="">
    <meta name="og:image" content="">
    <meta name="og:url" content="">

    <title>TITLE</title>

    <link rel="shortcut icon" href="favicon.ico">

    <!-- FONTS -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link rel="stylesheet"
        href="https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;600;900&display=swap">

    

</head>



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
@import "./css/flex.scss"

.texto-descricao {
    text-align: justify;
}

</style>
