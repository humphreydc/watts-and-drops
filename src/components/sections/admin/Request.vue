<script setup>
</script>

<template>
    <section class="px-4 sm:px-8">
        <!-- Desktop View -->
        <div class="hidden md:block w-full overflow-x-auto">
            <table class="w-full bg-white shadow-sm rounded-xl border-2 border-gray-200">
                <thead class="bg-gray-50">
                    <tr>
                        <th scope="col" class="th-style">STUDENT NO.</th>
                        <th scope="col" class="th-style">NAME</th>
                        <th scope="col" class="th-style">LOCATION</th>
                        <th scope="col" class="th-style">TYPE</th>
                        <th scope="col" class="th-style">DESCRIPTION</th>
                        <th scope="col" class="th-style">ACTION</th>
                    </tr>
                </thead>
                <tbody class="divide-y divide-gray-200">
                    <tr class="hover:bg-gray-50">
                        <td class="px-4 py-5 text-sm text-gray-900">2023506089</td>
                        <td class="px-4 py-5 text-sm text-gray-900 text-nowrap">Casey Lou Garcia</td>
                        <td class="px-4 py-5 text-sm text-gray-900">Room 411</td>
                        <td class="px-4 py-5 text-sm text-gray-900">Electricity</td>
                        <td class="px-4 py-5 text-sm text-gray-900 max-w-md leading-relaxed">The projector in Room 411 is currently not functioning. This affects the conduct of lectures and presentations that require visual materials.</td>
                        <td class="px-4 py-5">
                            <button class="text-xs text-white font-bold p-2 bg-green-500 cursor-pointer rounded-sm">MARK FIXED</button>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Mobile View -->
        <div class="md:hidden space-y-4">
            <div class="bg-white p-5 rounded-xl border-2 border-gray-200 shadow-sm space-y-3">
                <div class="flex justify-between items-start border-b border-gray-100 pb-2">
                    <div>
                        <p class="text-xs font-semibold text-gray-500">STUDENT NO</p>
                        <p class="text-sm font-bold text-gray-900">2023506089</p>
                    </div>
                    <span class="px-2 py-1 bg-amber-100 text-amber-700 text-[10px] font-bold rounded">ELECTRICITY</span>
                </div>
                
                <div>
                    <p class="text-xs font-semibold text-gray-500">NAME</p>
                    <p class="text-sm text-gray-900 font-medium">Casey Lou Garcia</p>
                </div>

                <div>
                    <p class="text-xs font-semibold text-gray-500">LOCATION</p>
                    <p class="text-sm text-gray-900">Room 411</p>
                </div>

                <div>
                    <p class="text-xs font-semibold text-gray-500">DESCRIPTION</p>
                    <p class="text-sm text-gray-600 leading-relaxed italic">"The projector in Room 411 is currently not functioning. This affects the conduct of lectures and presentations."</p>
                </div>

                <div class="flex justify-between pt-2 border-t border-gray-100">
                    <div>
                        <p class="text-[10px] font-semibold text-gray-400 mb-2">ACTION</p>
                        <button class="text-xs text-green-700 font-bold p-2 bg-green-200 hover:bg-green-400 cursor-pointer rounded-sm">MARK FIXED</button>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>