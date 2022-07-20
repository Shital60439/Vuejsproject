<template>
<div>
    <h1> HELLO from home component</h1>
    <!-- <h1>{{email}}</h1> -->
    <!-- <h1>{{msg}}</h1> -->

    <!-- <h1 v-if="show">Condition if-true part</h1>
    <h1 v-else>else part</h1>
     <button v-on:click="hello('data')">Click button</button> 
    <button v-on:click="display">Toogle</button> -->

    <table border="2">
        <tr>
            <td>Id</td><td>Name</td><td>Email</td>
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
    name:'Home-here',
    props:{
        data:String,
        msg:String
    },data(){
            return{
                //show:true
                users:[
                    {id:1,name:'peter',email:'peter@ola.com'},
                    {id:2,name:'sam',email:'sam@ola.com'},
                    {id:3,name:'tony',email:'tony@ola.com'},
                    {id:4,name:'bruse',email:'bruse@ola.com'},
                    {id:5,name:'harry',email:'harry@ola.com'},
                ]
            }
    },
    methods:{
       display(){
        this.show=!this.show
       }
    }

}
</script>