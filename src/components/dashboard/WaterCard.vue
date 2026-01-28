<script setup>

</script>

<template>
    <div class="card-border col-span-1 order-2 sm:order-3 flex flex-col gap-6">
        <div class="flex justify-between items-center">
            <div class="flex items-center gap-4">
                <div class="w-15 h-15 bg-blue-500 rounded-full p-1">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640" fill="">
                        <path d="M320 576C214 576 128 490 128 384C128 292.8 258.2 109.9 294.6 60.5C300.5 52.5 309.8 48 319.8 48L320.2 48C330.2 48 339.5 52.5 345.4 60.5C381.8 109.9 512 292.8 512 384C512 490 426 576 320 576zM240 376C240 362.7 229.3 352 216 352C202.7 352 192 362.7 192 376C192 451.1 252.9 512 328 512C341.3 512 352 501.3 352 488C352 474.7 341.3 464 328 464C279.4 464 240 424.6 240 376z"/>
                    </svg>
                </div>
                <p class="font-bold text-xl">Water</p>
            </div>
            <!-- optional update -->
            <span class="text-red-600 font-bold text-sm">+8% from last month</span> 
        </div>
        <div class="flex flex-col gap-4">
            <div class="flex flex-col gap-2">
                <p class="text-gray-600">Water usage:</p>
                <!-- changes in data here -->
                <div class="font-bold text-xl flex items-center">125
                    <span class="font-light text-lg text-gray-600 m-1">m³</span>
                </div>
            </div>
            <div class="percentage-bar">
                <div 
                    class="w-1/2 h-full bg-blue-400 border border-gray-200 
                    rounded-full flex items-center justify-center font-bold"
                >
                <!-- auto update -->
                45%
                </div>
            </div>
        </div>
    </div>    
</template>