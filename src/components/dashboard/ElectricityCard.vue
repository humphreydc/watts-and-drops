<script setup>

</script>

<template>
    <div class="card-border col-span-1 order-1 flex flex-col gap-6">
        <div class="flex justify-between items-center">
            <div class="flex items-center gap-4">
                <div class="w-10 h-10 border rounded-full"></div>
                <p class="font-bold text-xl">Electricity</p>
            </div>
            <!-- optional update -->
            <span class="text-green-600 font-bold text-sm">-8% from last month</span> 
        </div>
        <div class="flex flex-col gap-4">
            <div class="flex flex-col gap-2">
                <p class="text-gray-600">Electricity usage:</p>
                <!-- changes in data here -->
                <div class="font-bold text-xl flex items-center">345
                    <span class="font-light text-lg text-gray-600 m-1">kWh</span>
                </div>
            </div>
            <div class="percentage-bar">
                <div 
                    class="w-1/2 h-full bg-amber-400 border border-gray-200 
                    rounded-full flex items-center justify-center font-bold"
                >
                <!-- auto update -->
                45%
                </div>
            </div>
        </div>
    </div>    
</template>