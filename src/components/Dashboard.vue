<template>
    <div>
        <h1>Dashboard Component</h1>
        <User/>
        <Product/>
    </div>
  
</template>

<script>
import User from "./User.vue"
import Product from "./Product.vue"

export default {
    name : "Home",
    components:{
        User,
        Product
    }
}
</script>

<style scoped>
div{
    background-color:rgb(154, 176, 223) ;
    height: 500px;
}
</style>
