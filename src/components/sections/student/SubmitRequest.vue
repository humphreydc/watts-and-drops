<script setup>
</script>

<template>
    <section class="max-w-5xl w-full flex justify-center flex-col gap-12 px-4 sm:px-8">
        <div class="w-full sm:w-[80%]">
            <!-- input form -->
            <form action="" method="get" class="flex flex-col gap-6">
                <select class="input-border">
                    <option value="1">Select Room...</option>
                    <option value="2">304</option>
                    <option value="3">305</option>
                    <option value="4">306</option>
                    <option value="5">307</option>
                </select>

                <select class="input-border">
                    <option value="">Select Resource Type...</option>
                    <option value="2">304</option>
                    <option value="3">305</option>
                    <option value="4">306</option>
                    <option value="5">307</option>
                </select>

                <textarea 
                    name="detail" 
                    class="resize-none input-border placeholder-gray-400"
                    placeholder="Please describe the issue in detail..."
                ></textarea>

                <input 
                    type="submit" 
                    value="Submit to Maintenance"
                    class="bg-(--primary-color) text-white font-bold rounded-lg p-4 cursor-pointer"
                >
            </form> 
        </div>
        
        <div class="w-full">
            
            <div 
                class="bg-(--bg-color) rounded-xl border p-3 sm:p-6 border-gray-200 flex flex-col
                justify-between shadow-sm"
            >
                <h1 class="text-2xl font-bold">Maintenance Awareness</h1>
                <div class="flex flex-col py-4 gap-4 text-sm sm:text-base">
                    <p><b>Step 1: </b>Identify the specific room or area where the resource is failing.</p>
                    <p><b>Step 2: </b>Use the "Requests" tab to fill out the form. Your report will be visible on the system overview.</p>
                    <p><b>Step 3: </b>Keep an eye on the "Overview" tab. Once maintenance resolves the issue, the alert will be cleared.</p>
                </div>
            </div>
        </div>
    </section>
</template>