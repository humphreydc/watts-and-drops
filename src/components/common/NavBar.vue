<script setup>
const emit = defineEmits(['toggle-sidebar'])

</script>

<template>
    <nav class="w-full border border-gray-200">
        <div class="flex justify-between items-center py-2 px-4">
            <div class="flex items-center gap-4">
                <button 
                    @click="emit('toggle-sidebar')" 
                    class="hover:bg-gray-200 rounded-full text-3xl w-10 h-10 cursor-pointer"
                    type="button"
                >
                ☰
                </button>
                <p class="font-semibold text-xl">Dashboard</p>
            </div>
            <div class="flex items-center gap-4">
                <button class="w-10 h-10 border bg-black rounded-full cursor-pointer" type="button"></button>
                <button class="w-25 h-10 border rounded-full flex items-center px-2 cursor-pointer" type="button"></button>
            </div>
        </div>
    </nav>
</template>