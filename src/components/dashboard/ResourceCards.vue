<script setup>
import ElectricityCard from './ElectricityCard.vue';
import WaterCard from './WaterCard.vue';
import Graph from './Graph.vue';
</script>

<template>
    <section class="grid grid-cols-1 lg:grid-cols-2 gap-4 px-4 sm:px-8 py-4">
        <ElectricityCard/>
        <WaterCard/>
        <Graph/>
    </section>
</template>