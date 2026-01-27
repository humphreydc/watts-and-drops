<script setup>
const text = {
    title: "Resource Monitoring Dashboard",
    info: "Here's an overview of resource consumption this month.",
}

</script>

<template>
    <header class="px-4 sm:px-8 py-8 sm:py-8">
        <h1 class="text-2xl font-bold mb-2">{{ text.title }}</h1>
        <p class="text-gray-600">{{ text.info }}</p>
    </header>
</template>