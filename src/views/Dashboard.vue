<script setup>
import Navbar from '@/components/common/NavBar.vue';
import SidePanel from '@/components/dashboard/SidePanel.vue';
</script>

<template>
    <div class="">
       <div class="flex items-start">
            <div class="flex h-screen max-w-80 w-80">
                <SidePanel/>
            </div>
            <Navbar/> 
       </div>
       
    </div>
</template>