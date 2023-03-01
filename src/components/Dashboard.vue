<template>
    <div>
        <!-- <h1>Dashboard Component</h1> -->
        <p v-bind:style="{'color':`blue`}" v-html="rowHTML"></p>
        <!-- Template property start -->
        <h2 v-once>{{ name }}</h2>
        <h2>{{ name }}</h2>
        <h3>{{ a + b}}</h3>
        <h4>{{ ok ? "Yes" : "No" }}</h4>
        <button v-bind:disabled="disablebtn" v-on:click="updateText">Click me</button>
        <!-- Template property end -->

        <!-- class and style binding start -->
        <h5 c-bind:class="{display : show}">Class binding with objects</h5>
        <h5 c-bind:class="{display : show}">Class binding with Array</h5>
        <!-- class and style binding end -->
       
    </div>
    <User/>
    <Product/>
</template>

<script>
import User from "./User.vue"
import Product from "./Product.vue"

export default {
    name : "Home",
    data(){
        return{
            show : true
        }
    },
    components:{
        User,
        Product
    },
// Template property start
    data(){
        return {
            name : "Siddhant",
            a : 10, b : 20,
            ok : true,
            rowHTML : "<h1>Dashboard Component</h1>",
            disablebtn:true
        }
    },
    methods:{
       updateText(){
        this.name = "Peter"
       } 
    },
// Template property end
}
</script>

<style scoped>
div{
    background-color:rgb(154, 176, 223) ;
    height: 500px;
}
</style>
