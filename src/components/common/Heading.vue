<script setup>
defineProps({
    title: String,
    info: String
})
</script>

<template>
    <header class="px-4 sm:px-8 py-8 sm:py-8">
        <h1 class="text-2xl font-bold mb-2">{{ title }}</h1>
        <p class="text-gray-600">{{ info }}</p>
    </header>
</template>