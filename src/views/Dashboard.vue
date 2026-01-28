<script setup>
import { ref, computed } from 'vue';
import Navbar from '@/components/common/NavBar.vue';
import SidePanel from '@/components/common/SidePanel.vue';
import Heading from '@/components/common/Heading.vue';
import ResourceCards from '@/components/dashboard/ResourceCards.vue';
import Foot from '@/components/common/Foot.vue';
import Request from '@/components/sections/Request.vue';
import Resolution from '@/components/sections/Resolution.vue';

const isCollapsed = ref(true);
const currentSection = ref('overview');

const handleNavigation = (sectionId) => {
    currentSection.value = sectionId;
}

//load component
const getComponent = computed(() => {
    switch (currentSection.value) {
        case 'overview': return ResourceCards;
        case 'request': return Request;
        case 'resolution': return Resolution;
        default: return ResourceCards;
    }
});

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
        <div class="flex h-screen overflow-hidden">
            <!-- Sidebar Overlay for mobile -->
            <div v-if="!isCollapsed" @click="closeSidebar" class="fixed inset-0 bg-black/50 z-40 lg:hidden"></div>

            <div class="fixed inset-y-0 left-0 z-50 transition-transform duration-300 transform lg:relative lg:translate-x-0 h-full"
                :class="isCollapsed ? '-translate-x-full lg:translate-x-0' : 'translate-x-0'">
                <SidePanel :collapsed="isCollapsed" @close="closeSidebar" @select="handleNavigation" />
            </div>

            <div class="flex-1 flex flex-col min-w-0 h-full">
                <Navbar @toggle-sidebar="toggleSidebar" />
                <div class="flex-1 overflow-y-auto flex flex-col">
                    <Heading />
                    <main class="flex-1 mb-8">
                        <transition name="fade" mode="out-in">
                            <component :is="getComponent" />
                        </transition>
                    </main>
                    <Foot />
                </div>
            </div>
        </div>
    </div>
</template>