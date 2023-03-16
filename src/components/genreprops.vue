<script setup>
const genreprops = defineProps(['genre'])
</script>

<template >

    <li class="m-1">
        <input type="checkbox"  v-bind:id="genreprops.genre" class="hidden peer" required="" >
        <label v-bind:for="genreprops.genre" class="inline-flex justify-between items-center p-1  text-gray-500 bg-gray-200 rounded border-2 border-gray-200 cursor-pointer dark:hover:text-gray-300 dark:border-gray-700 peer-checked:border-blue-600 hover:text-gray-600 dark:peer-checked:text-gray-100 peer-checked:text-gray-600 hover:bg-gray-50 dark:text-gray-400 dark:bg-gray-800 dark:hover:bg-gray-700">
            <div class="block">
                <div class="w-full text-sm font-semibold">{{ genreprops.genre }}</div>
            </div>
        </label>
    </li>

</template>