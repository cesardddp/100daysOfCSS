<template>
  <main class>
    {{css_classes}}
    <nav>
      <ul class="nav-list" ref="1-ul">
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
      css_classes: []
    }
  },
  methods: {
    getClass(nameClass) {
      let styleSheet = document.styleSheets[0]
      let rules = styleSheet.cssRules
      
      for (let indice=0; indice<rules.length,indice++;) {
        if (rules[indice] === nameClass) return rules[indice];
      }
    },
  },
  mounted(){
    this.css_classes = this.getClass('.nav-list')
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "./css/flex.scss"
</style>
