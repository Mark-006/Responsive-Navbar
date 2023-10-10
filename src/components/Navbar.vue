<template>

    <div class="bg-gray-900 text-gray-100 py-3.5 px-6 shadow md:flex justify-between 
    items-center">
        <div class="flex items-center cursor-pointer">

            <span class="text-green-500 text-xl mr-1">

                <i class="bi bi-messenger"></i>

            </span>
           <h1 class="text-xl">Lish AI</h1>
        </div>
        <span @click="Menuopen()" class="absolute md:hidden right-6 top-1.5 cursor-pointer text-4xl">

            <i :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>

        </span>
        <ul class="md:flex md:items-center md:px-0 px-10 md:pb-0 pb-10 md:static absolute bg-gray-900
        md:w-auto w-full top-14 duration-700 ease-in"
        :class="[open ? 'left-0' : 'left-[-100%]']">


            <li class="md:mx-4 md:my-0 my-6" v-for="Link in Links">

                <a href="Link.Link" class="text-xl hover:text-blue-500">{{ Link.name }}</a>

            </li>
        <Button>
             Apply Now
        </Button>

        </ul>
    </div>
</template>

<script>
import {ref} from 'vue'
 import Button from './Button.vue'
    export default {
     
         components:{
            Button
         },
        setup(){
            let open = ref(false)
            let Links = [
                {name : "Home" , Link : "#"},
                {name : "Contact" , Link : "#"},
                {name : "Gallery" , Link : "#"},
                {name : "News & updates" , Link : "#"},
                
            ]

            function Menuopen(){
                open.value = !open.value
            }
            return{Links,open,Menuopen}
        }
    }
</script>

<style lang="scss" scoped>

</style>