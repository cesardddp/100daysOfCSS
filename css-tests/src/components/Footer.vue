<template>
  <footer >
    <p >
      <a  href="#">Voltar lá em cima!</a>
    </p>
    <p >
      &copy;{{ year }} Mantido por
      <a
        href="https://github.com/cesardddp"
        target="_blank"
      >cesardddp</a> &middot;
    </p>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
  props: {
  },
  data() {
    return{
      year: 0
    }
  },
  mounted() {
    let date = new Date();
    this.year = date.getFullYear()
    
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
