<script setup>

</script>

<template>
    <div class="card-border col-span-1 order-1 flex flex-col gap-6">
        <div class="flex justify-between items-center">
            <div class="flex items-center gap-4">
                <div class="w-15 h-15 bg-amber-500 rounded-full p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640">
                        <path d="M434.8 54.1C446.7 62.7 451.1 78.3 445.7 91.9L367.3 288L512 288C525.5 288 537.5 296.4 542.1 309.1C546.7 321.8 542.8 336 532.5 344.6L244.5 584.6C233.2 594 217.1 594.5 205.2 585.9C193.3 577.3 188.9 561.7 194.3 548.1L272.7 352L128 352C114.5 352 102.5 343.6 97.9 330.9C93.3 318.2 97.2 304 107.5 295.4L395.5 55.4C406.8 46 422.9 45.5 434.8 54.1z"/>
                    </svg>
                </div>
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