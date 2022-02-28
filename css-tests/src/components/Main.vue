<template>
  <main class>
    css:{{gridStyle}}
    <nav>
      <ul class="" :style="gridStyle">
        <li v-for="(index, l) in nav_list" :key="index">
          <a href="#">{{ l }}</a>
        </li>
        <li>
          <a href="#">nice</a>
        </li>
        <li>
          <a href="#">realy nice content</a>
        </li>
        <li>
          <a href="#">i don now, i dont like it</a>
        </li>
        <li>
          <a href="#">ok</a>
        </li>
        <li>
          <a href="#">is not home</a>
        </li>
        <li>
          <a href="#">home</a>
        </li>
      </ul>
    </nav>
  </main>
</template>

<script>
export default {
  name: 'Main',
  props: {
  },
  data() {
    return {
      gridStyle:{
        display: "flex",
        gap: "1rem"
      }
    }
  },
  methods: {
    
  },
  mounted(){
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "./css/flex.scss";

</style>
