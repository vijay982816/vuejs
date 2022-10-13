<template>
<div >

                <div class='py-12 bg-gray-700 transition duration-150 ease-in-out z-10 absolute top-0 right-0 bottom-0 left-0  ' id="modal">





   <form  class="add-form container mx-auto w-11/12 md:w-2/3 max-w-lg">
  

    <div class="form-control">
           <label class="text-white text-sm font-bold leading-tight tracking-normal">Name</label>
                            <input id="name" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Hitesh"  v-model="name" name='name' />



    </div>
    <div class="form-control">
           <label class="text-white text-sm font-bold leading-tight tracking-normal">Email</label>
                            <input id="name" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. name@gmail.com"  v-model="email" name='email' />



    </div>
  
    <div class="form-control">
           <label class="text-white text-sm font-bold leading-tight tracking-normal">phone</label>
                            <input id="email" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. 9898989898 "  v-model="phone" name='phone' />



    </div>

      <div class="form-control">
           <label class="text-white text-sm font-bold leading-tight tracking-normal">City</label>
                            <input id="city" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Jaipur"  v-model="city" name='city' />



    </div>




<button class="btn btn-block bg-white px-5 py-3 rounded-lg " @click="adduser" >add user</button>
  </form>

                </div>
         





                    <div >

                <div class='py-12 bg-gray-700 transition duration-150 ease-in-out z-10 absolute top-0 right-0 bottom-0 left-0 ' id="modal">




              





                    <div role="alert" class="container mx-auto w-11/12 md:w-2/3 max-w-lg">
                        <div class="relative py-8 px-5 md:px-10 bg-white shadow-md rounded border border-gray-400">
                       
                            <h1 class="text-gray-800 font-lg font-bold tracking-normal leading-tight mb-4">Enter User Details</h1>
                            <label htmlFor="name" class="text-gray-800 text-sm font-bold leading-tight tracking-normal">User Name</label>
                            <input id="name" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Hitesh"  v-model="name" name='name' />






                            <label htmlFor="email" class="text-gray-800 text-sm font-bold leading-tight tracking-normal">Email</label>
                            <input id="email" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border"  placeholder="Ex. Hitesh@gmail.com"  v-model="email" name='email' />

                            <label htmlFor="email" class="text-gray-800 text-sm font-bold leading-tight tracking-normal">city</label>
                            <input id="email" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border"  placeholder="Ex.jaipur"  v-model="city" name='city' />

                            <label htmlFor="email" class="text-gray-800 text-sm font-bold leading-tight tracking-normal">phone</label>
                            <input id="email" class="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border"  placeholder="Ex. 9898989898"  v-model="phone" name='phone' />




                            






                            <div class="flex items-center justify-start w-full">
                                <button class="focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-indigo-700 transition duration-150 ease-in-out hover:bg-indigo-600 bg-indigo-700 rounded text-white px-8 py-2 text-sm"
                                @click="adduser"
                                
                                >Submit</button>



                                <RouterLink to="/" class="focus:outline-none focus:ring-2 focus:ring-offset-2  focus:ring-gray-400 ml-3 bg-gray-100 transition duration-150 text-gray-600 ease-in-out hover:border-gray-400 hover:bg-gray-300 border rounded px-8 py-2 text-sm" >Cancel</RouterLink>

                            </div>
                           
                        </div>
                    </div>
                </div>

            </div>





                   </div>

</template>

<script>
export default {
name:"UpdateUser",

 data (){
            return {
                name : '',
                email : '',
                phone : '',
                city : '',
                user:[]

            }
        },
        
created(){


    this.id=this.$route.params._id
    // console.log('myid is ',this.id),
   

},

methods:{

async adduser (){

console.log(this.name,this.email,this.phone,this.city)




//  const addedUser = await fetch('https://vijay982816-curd-brained-rv996pr4qpph55r-3000.githubpreview.dev/employee/Register',



// {
//     method: 'POST',
//     headers: {
//       'Accept': 'application/json',
//       'Content-Type': 'application/json'
//     },
//     body: JSON.stringify({name:this.name,phone:this.phone,email:this.email,city:this.city})
//   }



// )
//   .then((async (response) => await response.json()))
//   .catch((error) => console.log(error.message));


//   console.log(addedUser)



//   this.$router.push('/') 




// this.adduser()

this.getuser()

}

,

 async getuser (){

console.log('get data')

    
const userdata = await fetch(`https://vijay982816-curd-brained-rv996pr4qpph55r-3000.githubpreview.dev/employee/getEmployee/${this.$route.params.id}`)


 let user= await userdata.json()

 this.name=user.name;
 this.email=user.email;
 this.phone=user.phone;
 this.city=user.city;

console.log(userdata)

    


}

}

}
</script>

<style>

</style>