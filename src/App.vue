<template>
  <Dashboard/>
  <Databinding/>
  <h1>{{ title }}</h1>
  <Props v-bind:users = "users" v-on:changeTitle="updateTitle($event)"/>
  <Signup/>
  
</template>

<script>
import Dashboard from './components/Dashboard.vue'
import Databinding from './components/Databinding.vue';
import Props from './components/Props.vue';
import Signup from './components/Signup.vue';

export default {
  name: 'App',
  components: {
    Dashboard,
    Databinding,
    Props,
    Signup
  },
  data(){
    return {users:[
      {name:"anil",email:"amnil@gmail.com"},
      {name:"karim",email:"karim@gmail.com"}
    ]}
  },
  data(){
    return {title:"props tutorial"}
  },
  methods:{
    updateTitle(title){
      this.title = title
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
