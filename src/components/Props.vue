<template>
    <div>
    <h1>Props in Vue parent to child</h1>
    <h4 v-for="user in users" :key="user.name">{{ user.name }} --- {{ user.email }}</h4>
    <h1>Props in Vue child to parent</h1>
    <button v-on:click="updateTitle">Update parent title</button>
</div>
</template>

<script>
export default{
    name:"Props",
    props:['users'],
    methods:{
        updateTitle(){
            this.$emit('changeTitle','Parent updated')
        }
    }
}
</script>

<style scoped>
div{
    background-color: rgba(48, 9, 87, 0.747);
    height: 150px;
}
</style>