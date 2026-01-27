<script setup>
import { ref } from 'vue';

defineProps({
  collapsed: Boolean
});

const items = ref([
    { id: "overview", label: "Overview", href: "#overview" },
    { id: "request", label: "Request", href: "#request" },
    { id: "awareness", label: "Awareness", href: "#awareness" } ,
]);

const text = {
    title: "Watts & Drops",
    sub: "Navigation",
};

const activeItemId = ref("overview");

const isActive = (item) => {
    activeItemId.value = item.id
};
</script>

<template>
    <aside 
        class="flex h-screen bg-(--bg-color) flex-col 
        shadow-sm border border-gray-200 gap-12 p-3 px-4 z-50
        sticky"
    >
        <div class="flex items-center gap-3">
            <img class="w-6" src="/src/assets/images/logo.png" alt="logo">
            <p v-if="!collapsed" class="text-(--primary-color) font-bold text-xl mr-6">{{ text.title }}</p>
        </div>
        <div class="">
            <p v-if="!collapsed" class="text-sm text-gray-500 py-4">{{ text.sub }}</p>
            <ul class="flex flex-col gap-2">
                <li 
                    v-for="item in items" 
                    :key="item.id"
                    @click="isActive(item)"
                    class="text-base cursor-pointer rounded-sm py-1 px-3" 
                    :class="activeItemId === item.id ? 'bg-(--primary-color)' : 'bg-white'"
                >
                    <span v-if="!collapsed">{{ item.label }}</span>
                </li>
            </ul>
        </div>
    </aside>
</template>