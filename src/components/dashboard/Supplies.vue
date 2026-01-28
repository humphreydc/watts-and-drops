<script setup>

</script>

<template>
    <div class="card-border col-span-1 order-2 sm:order-3 flex flex-col gap-6">
        <div class="flex justify-between items-center">
            <div class="flex items-center gap-4">
                <div class="w-15 h-15 bg-red-500 rounded-full p-2">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 640 640">
                        <path d="M240 64L320 64L320 120C320 133.3 330.7 144 344 144L424 144C437.3 144 448 133.3 448 120L448 64L528 64C554.5 64 576 85.5 576 112L576 528C576 554.5 554.5 576 528 576L419.2 576C427.4 561.9 432 545.5 432 528L432 368C442 354.6 448 338 448 320L448 288C448 243.8 412.2 208 368 208L192 208L192 112C192 85.5 213.5 64 240 64zM64 400L384 400L384 528C384 554.5 362.5 576 336 576L112 576C85.5 576 64 554.5 64 528L64 400zM80 256L368 256C385.7 256 400 270.3 400 288L400 320C400 337.7 385.7 352 368 352L80 352C62.3 352 48 337.7 48 320L48 288C48 270.3 62.3 256 80 256z"/>
                    </svg>
                </div>
                <p class="font-bold text-xl">Supplies</p>
            </div>
            <!-- optional update -->
            <span class="text-red-600 font-bold text-sm">+10% from last month</span> 
        </div>
        <div class="flex flex-col gap-4">
            <div class="flex flex-col gap-2">
                <p class="text-gray-600">Supply usage:</p>
                <!-- changes in data here -->
                <div class="font-bold text-xl flex items-center">90
                    <span class="font-light text-lg text-gray-600 m-1"></span>
                </div>
            </div>
            <div class="percentage-bar">
                <div 
                    class="w-1/2 h-full bg-red-400 border border-gray-200 
                    rounded-full flex items-center justify-center font-bold"
                >
                <!-- auto update -->
                45%
                </div>
            </div>
        </div>
    </div>    
</template>