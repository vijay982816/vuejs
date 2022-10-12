<template>
  <div>
    <h1>Getting All User Using Vue js</h1>
    <button @click="getUsers"  >Get the users </button>


     <!-- <button class="outline-primary">Button</button> -->

    <!-- <h3 v-for = "(name,index) in names" :key ="name">{{index}} {{name}}</h3> -->

 <table v-if="users.length > 0">
  <tr>
    <th>id</th>
    <th>name</th>
    <th>username</th>
    <th>email</th>
    <th>city</th>
    <th>ZipCode</th>
  </tr>

  <tr  v-for = "(name) in users" :key ="name" >


    <td>{{name.id}}</td>
    <td>{{name.name}}</td>
       <td>{{name.username}}</td>
     <td>{{name.email}}</td>
     <td>{{name.address.city}}</td>
     <td>{{name.address.zipcode}}</td>

  </tr>
 
</table>

  </div>


 
</template>

<script>



  export default {
      name : "UsingBootstrap",
    data() {
      return {
  users:[]
    
   
      }
    },
    created(){
// this.getUsers()
    },
    methods:{
       async getUsers(){

         const getingUsers = await fetch('https://jsonplaceholder.typicode.com/users')
        .then(async Response=>{
this.users=await Response.json();

})
.catch(error=>console.log(error.message))

}
    }
  }
</script>


