<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false);
</script>

<template>
    <nav class="w-full border border-gray-200">
        <div class="flex items-center py-2 px-4 gap-4">
            <button @click="isMenuOpen = !isMenuOpen" class="text-3xl w-10 cursor-pointer">
                {{ isMenuOpen ? '✕' : '☰' }}
            </button>
            <p class="font-semibold text-xl">Dashboard</p>
        </div>
    </nav>
</template>