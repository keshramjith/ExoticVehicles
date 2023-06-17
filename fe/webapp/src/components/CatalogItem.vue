<script setup lang="ts">
const props = defineProps({
    title: String,
    description: String,
    availability: Boolean,
    price: Number
})
</script>

<template>
    <div class="m-2 p-6 w-96 h-52 max-w-lg mx-auto bg-white rounded-xl shadow-md items-center">
        <p class="font-semibold text-lg">{{ title }}</p>
        <p class="text-xs">img</p>
        <p class="text-sm">{{  description }}</p>
        <div class="flex justify-between items-center">
            <div v-if="availability === true" class="p-1.5 max-w-sm bg-green-400 rounded-full">
                <p class="text-xs">Available</p>
            </div>
            <div v-else class="p-1.5 max-w-sm bg-red-400 rounded-full">
                <p class="text-xs">Taken</p>
            </div>
            <p class="text-lg">${{ price }}/day</p>
        </div>
        <button v-if="availability===true" class="p-1 my-2 bg-cyan-400 rounded-lg">Register interest</button>
    </div>
</template>

<style></style>