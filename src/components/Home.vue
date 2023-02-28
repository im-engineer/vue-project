<template>
    <div>
       <h1 v-if="show">Hello from home component</h1> 
       <h1 v-else>else condition</h1>
       <button v-on:click="display">Toggle Element</button> 
        <h2>{{ data }}</h2>
        <h2>{{ msg }}</h2>
        <button v-on:click="hello('hello call')">Call Hello Function</button>
    </div>
</template>

<script>
export default {
    name:'Home',
    props : {
        data : String,
        msg : String
    },
    methods:{
        hello(data){
            // console.log('Hello from home component')
            alert(data)
        }
    },

    //if condition to show data
    data(){
        return {show:true} 
    },
    methods:{
        display(){
            this.show =! this.show
        }
    }
}
</script>