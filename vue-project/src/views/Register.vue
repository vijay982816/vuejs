<template>
<div >

                <div className='py-12 bg-gray-700 transition duration-150 ease-in-out z-10 absolute top-0 right-0 bottom-0 left-0  ' id="modal">





   <form @submit="onSubmit" class="add-form container mx-auto w-11/12 md:w-2/3 max-w-lg">
  

    <div class="form-control">
           <label className="text-white text-sm font-bold leading-tight tracking-normal">Name</label>
                            <input id="name" className="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Hitesh"  v-model="name" name='name' />



    </div>
    <div class="form-control">
           <label className="text-white text-sm font-bold leading-tight tracking-normal">Name</label>
                            <input id="name" className="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Hitesh"  v-model="name" name='name' />



    </div>
  
    <div class="form-control">
           <label className="text-white text-sm font-bold leading-tight tracking-normal">Email</label>
                            <input id="email" className="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. name@gmail.com"  v-model="email" name='email' />



    </div>

      <div class="form-control">
           <label className="text-white text-sm font-bold leading-tight tracking-normal">City</label>
                            <input id="city" className="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Jaipur"  v-model="city" name='city' />



    </div>

      <div class="form-control">
           <label className="text-white text-sm font-bold leading-tight tracking-normal">Password</label>
                            <input id="password" className="mb-5 mt-2 text-gray-600 focus:outline-none focus:border focus:border-indigo-700 font-normal w-full h-10 flex items-center pl-3 text-sm border-gray-300 rounded border" placeholder="Ex. Password@123"  v-model="Password" name='password' />



    </div>

<input type="submit" value="Save Information" class="btn btn-block bg-white px-3 oy-3" />
  </form>

                </div>
                </div>




</template>

<script>
export default {
name:"Register",
 data (){
            return {
                name : '',
                email : '',
                phone : null,
                city : '',

            }
        },

methods:{



}

}
</script>

<style>

</style>