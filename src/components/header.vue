<script setup>
import gen from './genre.vue'
</script>
<template>
    <!-- <div class="p-2 bg-gray-800 ">
        <div class="flex">
            <div class="my-auto mt-1">
                <i id="homeButton" class="fa fa-bars" style="font-size:large; color:rgb(255, 255, 255);"></i>    
            </div>    
            <h1 class="mt-1 ml-3">
            Basement Wibu
            </h1>
        </div>
    </div> -->
        
    <div id="sideBar" class="mx-auto md:px-20 px-0 py-1 md:flex">
        <div class="p-2 grid-flow-row auto-rows-max flex gap-2 w-1/2">
            <gen />
        </div>


    <div class="md:w-1/2 w-full my-2">      
        <form class=" bg-gray-800 p-1 rounded">   
            <div class="flex flex-row ">
                <input type="text" class="w-full px-5 mr-2 rounded bg-gray-700">
                <div class="">
                <i style="font-size:large; color:rgb(255, 255, 255);" class="fa-solid fa-magnifying-glass mt-1"></i>
                </div>
            </div>
        </form>
    </div>
</div>

</template>