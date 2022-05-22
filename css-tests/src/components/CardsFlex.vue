<template>
    <p>css flex parent:{{ section }}</p>
    <p>css flex-items: {{ card }}</p>

    <input type="checkbox" v-model="wrap" > wrap
    <br>
    <input type="checkbox" v-model="shrink" > shrink
    <input type="checkbox" v-model="grow" > grow
    <select name="" id="" v-model="basis">
        <option value="auto">auto</option>
        <option value="1">1</option>
        <option value="0">0</option>
    </select> basis
    <br>
    flex: <input type="text" v-model="flex" > 
<section :style="section">
    <article :style="card">
        <h3><b>Nice Stuf</b></h3>
        <p> sequi consequatur, eveniet aliquid.</p>
    </article>
    <article :style="card">
        <h3><b> Stuf</b></h3>
        <p> consectetur, adipisicing elit.</p>
    </article>
    <article :style="card">
        <h3><b>dumb Stuf</b></h3>
        <p>Lorem ipsum dolor sit ipsa sequi consequatur, eveniet aliquid.</p>
    </article>
</section>
</template>

<script>
export default {
    name: 'CardFlex',
    props: {
    },
    data() {
        return {
            section: {
                display: "flex",
                gap: "1rem",
                "flex-wrap": "wrap"
            },
            card: {
                "flex-shrink": 1,
                "flex-grow": 0,
                flex:"",
                "flex-basis": "none",
            },
            nav_list: ["teste", "nice", "realy nice content", "i don now, i dont like it", "ok", "is not home"],
            shrink: true,
            grow: false,
            wrap: false,
            basis:'auto',
            flex:"",

        }
    },
    methods: {

    },
    mounted() {
    },
    watch: {
        shrink() {
            this.card["flex-shrink"] = this.shrink ? 1 : 0
        },
        grow() {
            this.card["flex-grow"] = this.grow ? 1 : 0
        },
        wrap() {
            this.section["flex-wrap"] = this.wrap ? 'wrap' : 'nowrap'
        },
        basis() {
            this.card["flex-basis"] = this.basis
        },
    
        flex() {
            this.card["flex"] = this.flex
        }
    }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
* {
    box-sizing: border-box;
}
article{
    background-color: greenyellow;
    h3,p{
        font-size: 0.80em;;
    }
}
section{
    width: 120%;
    border: 5px solid firebrick;
}
</style>
