<template>
    <p>css flex parent:{{gridStyle}} </p>
    <p>css flex-items: {{itemStyle}}</p>
    
    <input type="checkbox" v-model="shrink" > shrink
    <input type="checkbox" v-model="grow" >grow
    <input type="checkbox" v-model="wrap" >wrap
    <nav>
      <ul class="" :style="gridStyle">
        <li v-for="(l, index) in nav_list" :key="index" :style="itemStyle">
          <a href="#">{{ l }}</a>
        </li>
        
        <li>
          <a href="#">home</a>
        </li>
      </ul>
    </nav>
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
        gap: "1rem",
        "flex-wrap":"wrap"
      },
      itemStyle:{
        "flex-shrink":1,
        "flex-grow":0,
      },
      nav_list:["teste","nice","realy nice content","i don now, i dont like it","ok","is not home"],
      shrink:true,
      grow:false,
      wrap:true,

    }
  },
  methods: {
    
  },
  mounted(){
  },
  watch:{
    shrink(){
      this.itemStyle["flex-shrink"]= this.shrink ? 1 : 0
    },
    grow(){
      this.itemStyle["flex-grow"]= this.grow ? 1 : 0
    },
    wrap(){
      this.gridStyle["flex-wrap"]= this.wrap ? 'wrap' : 'nowrap'
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import "./css/flex.scss";
*{
  box-sizing:border-box;
}
nav{
  // width: 90vh;
}
</style>
