<script setup>
import { ref } from 'vue';
import Navbar from '@/components/common/NavBar.vue';
import SidePanel from '@/components/common/SidePanel.vue';
import Heading from '@/components/common/Heading.vue';
import ResourceCards from '@/components/dashboard/ResourceCards.vue';
import Foot from '@/components/common/Foot.vue';

const isCollapsed = ref(false);

const toggleSidebar = () => {
  isCollapsed.value = !isCollapsed.value
}
</script>

<template>
    <div class="w-full">
       <div class="flex min-h-screen">
            <div class="flex h-screen">
                <SidePanel :collapsed="isCollapsed" />
            </div>
            <div class="flex-1">
                <Navbar @toggle-sidebar="toggleSidebar" /> 
                <Heading/>
                <main>
                    
                       <ResourceCards/> 
                    
                </main>
            </div>
       </div>
       <footer>
            <Foot/>
       </footer>
    </div>
</template>