<script setup lang="ts">
const props = defineProps({
    title: String,
    description: String,
    availability: Boolean,
    price: Number
})
</script>

<template>
    <div class="p-6 max-w-lg mx-auto bg-white rounded-xl shadow-md items-center">
        <p class="font-semibold text-lg">{{ title }}</p>
        <p class="text-xs">img</p>
        <p class="text-sm">{{  description }}</p>
        <div class="flex content-between">
            <div v-if="availability === true" class="p-1 max-w-sm mx-auto bg-green-400 rounded-md">
                <p class="text-base">Available</p>
            </div>
            <div v-else class="p-1 max-w-sm mx-auto bg-red-400 rounded-md">
                <p class="text-base">Taken</p>
            </div>
            <p class="text-lg">${{  price }}</p>
        </div>
        <button v-if="availability===true" class="p-1 m-2 bg-blue-500 rounded-lg">Register interest</button>
    </div>
</template>

<style></style>