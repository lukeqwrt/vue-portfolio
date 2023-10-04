<script setup>
import { ref } from 'vue'

const navitems = ref([
  { name: 'Home' },
  { name: 'About' },
  { name: 'Projects' },
  { name: 'Contact' },
])

</script>

<template>
    <ul class="">
        <li 
            v-for="nav in navitems" :key="nav" 
            class="navitem flex justify-center items-center cursor-pointer group"
            >
            <div class="relative  py-3 md:py-2 text-md cursor-pointer font-[600]">
                {{ nav.name }}
                <span class="underline absolute bottom-0 left-[50%] translate-x-[-50%] block h-[2px] bg-black duration-200 w-0 group-hover:w-full"></span>
            </div>
            
        </li>
    </ul>
</template>