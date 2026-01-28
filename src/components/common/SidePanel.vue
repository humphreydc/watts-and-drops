<script setup>
import { ref } from 'vue';

defineProps({
    collapsed: Boolean
});

const emit = defineEmits(['close']);

const items = ref([
    { 
        id: "overview", 
        label: "Overview", 
        icon: `<svg class="w-6 h-6" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15v4m6-6v6m6-4v4m6-6v6M3 11l6-5 6 5 5.5-5.5"/>
</svg>`
    },
    { 
        id: "request", 
        label: "Request", 
        icon: `<svg class="w-6 h-6" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 4h3a1 1 0 0 1 1 1v15a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1V5a1 1 0 0 1 1-1h3m0 3h6m-6 5h6m-6 4h6M10 3v4h4V3h-4Z"/>
</svg>`
    },
    { 
        id: "resolution", 
        label: "Resolution", 
        icon: `<svg class="w-6 h-6" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" width="24" height="24" fill="none" viewBox="0 0 24 24">
  <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z"/>
</svg>`
    },
]);

const text = {
    title: "Watts & Drops",
    sub: "Navigation",
};

const activeItemId = ref("overview");

const isActive = (item) => {
    activeItemId.value = item.id;
    emit('select', item.id);
    emit('close');
};
</script>

<template>
    <aside class="flex h-screen bg-(--bg-color) flex-col 
        shadow-sm border border-gray-200 gap-12 p-3 px-4 z-50
        sticky" :class="collapsed ? 'w-20' : 'w-64'">
        <div class="flex items-center gap-3" :class="collapsed ? 'justify-center' : 'justify-between'">
            <div class="flex items-center gap-3">
                <img class="w-6" src="/src/assets/images/logo.png" alt="logo">
                <p v-if="!collapsed" class="text-(--primary-color) font-bold text-xl">{{ text.title }}</p>
            </div>
            <button v-if="!collapsed" @click="emit('close')" class="lg:hidden p-2 text-xl text-gray-500 cursor-pointer">
                ✕
            </button>
        </div>
        <div class="overflow-y-auto">
            <p v-if="!collapsed" class="text-sm text-gray-500 py-4">{{ text.sub }}</p>
            <ul class="flex flex-col gap-2">
                <li v-for="item in items" :key="item.id" @click="isActive(item)"
                    class="text-base cursor-pointer rounded-sm py-2 px-3 flex items-center gap-3 transition-colors"
                    :class="[
                        activeItemId === item.id 
                            ? (collapsed ? 'text-(--primary-color)' : 'bg-(--primary-color) text-white') 
                            : 'text-gray-600 hover:bg-gray-100',
                        collapsed ? 'justify-center px-0' : ''
                    ]">
                    <div v-html="item.icon" class="flex-shrink-0" :class="activeItemId === item.id && collapsed ? 'text-(--primary-color)' : ''"></div>
                    <span v-if="!collapsed" class="whitespace-nowrap">{{ item.label }}</span>
                </li>
            </ul>
        </div>
    </aside>
</template>