<template>
    <div>
        <h1>Data binding in vue</h1>
        <p>{{ message }}</p>
        <input type="text" v-model="message"/>
    </div>
</template>

<script>
export default{
    name : "Data bind",
    data(){
        return {
            message : "Hi"
        }
    }
}
</script>

<style scoped>
div{
    background-color: rgba(125, 19, 224, 0.747);
    height: 150px;
}
</style>
