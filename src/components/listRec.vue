<script lang="ts">
export default {
    props: {
        mangaid: String,
        name: String,
        desc: String,
        image: String,
        genre: String
    }
}

</script>
<template>
<div id="showList">
    <div v-bind:id="mangaid" class=" flex flex-col p-1 ">
        <img class="h-50 w-full rounded" v-bind:src="image"  alt="">
        <div class="mx-2">
            <h1 class="text-lg">{{ name }}</h1>
            
            <p class="overflow-y-auto md:h-12 h-24 hover:h-auto text-sm">
                {{ desc }}
            </p>
        </div>    
    </div>
</div>
</template>