<script setup>
import { ref } from 'vue';

const items = ref([
    { id: "overview", label: "Overview", href: "#overview" },
    { id: "request", label: "Request", href: "#request" },
    { id: "awareness", label: "Awareness", href: "#awareness" } ,
]);

const text = {
    title: "Watts & Drops",
    sub: "Navigation",
};

const isUserAdmin = ref(false);

</script>

<template>
    <section class="h-full w-full bg-(--bg-color) shadow-sm py-3 px-4 z-50">
        <div class="flex items-center gap-4">
            <img class="w-6" src="/src/assets/images/logo.png" alt="logo">
            <p class="text-(--primary-color) font-bold text-xl">{{ text.title }}</p>
        </div>
        <p>{{ text.sub }}</p>
        <ul class="mt-4">
            <li 
                class="text-base cursor-pointer my-3" 
                :key="item.id"
                v-for="item in items" 
                :href="item.href"
            >
                {{ item.label }}
            </li>
        </ul>
    </section>
</template>