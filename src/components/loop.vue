<template>
    <div>
        <h1>
            For loop in vue js
        </h1>
        <table>
            <tr>
                <td>Id</td>
                <td>Name</td>
                <td>Email</td>
            </tr>
            <tr v-for="user in users" :key="user.id">
                <td>{{user.id}}</td>
                <td>{{user.name}}</td>
                <td>{{user.email}}</td>
            </tr>       
        </table>
    </div>
</template>
<script>
export default{
    name : "Loop",
    data(){
        return{
            users:[
                { id: 1, name:"siddhant", email: "siddhant@gmail.com" },
                { id: 2, name: "ramesh", email: "ramesh@gmail.com" },
                { id: 3, name: "suresh", email: "suresh@gmail.com" },
                { id: 4, name: "mahesh", email: "mahesh@gmail.com" },
                { id: 5, name: "brijesh", email: "brijesh@gmail.com" },
                { id: 6, name: "ganesh", email: "ganesh@gmail.com" },
            ]
        }
    }
}
</script>
