<template>
    <div>
        <p>Form with checkbox and radio button</p>
        <input type="text" placeholder="Enter your name" v-model="signup.username"/> <br><br>
        <input type="password" placeholder="Enter your password" v-model="signup.password"/> <br><br>
        <p>Select Hobbies : </p>
        <input type="checkbox" id="cricket" value="cricket" v-model="signup.hobbies"/>
        <label for="cricket">Cricket</label>
        <input type="checkbox" id="football" value="football" v-model="signup.hobbies"/>
        <label for="football">Football</label> <br>
        <p>Select Gender : </p>
        <input type="radio" id="male" value="male" v-model="signup.gender"/>
        <label for="male">Male</label>
        <input type="radio" id="female" value="female" v-model="signup.gender"/>
        <label for="female">Female</label> <br><br>
        <button v-on:click="signupUser">Signup</button>
    </div>
</template>

<script>
export default{
 name:"Signup",
 data(){
    return {
        signup : {
            username : null,
            password : null,
            hobbies : [],
            gender : []
        }
    }
 },
 methods:{
    signupUser(){
        console.warn(this.signup)
    }
 }
}
</script>

<style scoped>
div{
    background-color: rgb(138, 50, 221);
    height: 300px;
}
</style>