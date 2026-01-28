<script setup>
</script>

<template>
    <section class="px-4 sm:px-8">
        <div class="w-full overflow-x-auto">
            <table class="w-full bg-white shadow-sm rounded-lg">
                <thead class="bg-gray-50">
                    <tr>
                        <th scope="col" class="th-style">Student no.</th>
                        <th scope="col" class="th-style">Name</th>
                        <th scope="col" class="th-style">Location</th>
                        <th scope="col" class="th-style">Type</th>
                        <th scope="col" class="th-style">Description</th>
                        <th scope="col" class="th-style">Reported</th>
                        <th scope="col" class="th-style">Resolved</th>
                    </tr>
                </thead>
                <tbody class="divide-y divide-gray-200">
                    <!-- data here -->
                    <tr class="hover:bg-gray-50 transition-colors">
                        <td class="px-4 py-5 text-sm text-gray-900">2023506089</td>
                        <td class="px-4 py-5 text-sm text-gray-900">Casey Lou Garcia</td>
                        <td class="px-4 py-5 text-sm text-gray-900">Room 411</td>
                        <td class="px-4 py-5 text-sm text-gray-900">Electricity</td>
                        <td class="px-4 py-5 text-sm text-gray-900 max-w-md leading-relaxed">The projector in Room 411 is currently not functioning. This affects the conduct of lectures and presentations that require visual materials.</td>
                        <td class="px-4 py-5 text-sm text-red-500 font-medium">09:00 AM</td>
                        <td class="px-4 py-5 text-sm text-green-500 font-medium">10:40 AM</td>
                    </tr>
                    
                </tbody>
            </table>
    </div>
    </section>
</template>