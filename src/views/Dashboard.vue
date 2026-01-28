<script setup>
import { ref } from 'vue';
import Navbar from '@/components/common/NavBar.vue';
import SidePanel from '@/components/common/SidePanel.vue';
import Heading from '@/components/common/Heading.vue';
import ResourceCards from '@/components/dashboard/ResourceCards.vue';
import Foot from '@/components/common/Foot.vue';

const isCollapsed = ref(true);

const toggleSidebar = () => {
  isCollapsed.value = !isCollapsed.value
}

const closeSidebar = () => {
  if (window.innerWidth < 1024) {
    isCollapsed.value = true
  }
}
</script>

<template>
    <div class="w-full relative overflow-x-hidden">
       <div class="flex min-h-screen">
            <!-- Sidebar Overlay for mobile -->
            <div 
                v-if="!isCollapsed" 
                @click="closeSidebar"
                class="fixed inset-0 bg-black/50 z-40 lg:hidden"
            ></div>
            
            <div 
                class="fixed inset-y-0 left-0 z-50 transition-transform duration-300 transform lg:relative lg:translate-x-0"
                :class="isCollapsed ? '-translate-x-full lg:translate-x-0' : 'translate-x-0'"
            >
                <SidePanel :collapsed="isCollapsed" @close="closeSidebar" />
            </div>

            <div class="flex-1 flex flex-col min-w-0">
                <Navbar @toggle-sidebar="toggleSidebar" /> 
                <Heading/>
                <main class="flex-1">
                    <ResourceCards/> 
                </main>
                <footer>
                    <Foot/>
                </footer>
            </div>
       </div>
    </div>
</template>