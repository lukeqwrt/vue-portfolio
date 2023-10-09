<script setup>
import { ref } from 'vue'
import { useDark, useToggle } from "@vueuse/core"

const isDark = useDark()
const toggleDark = useToggle(isDark)

const navitems = ref([
  { name: 'Home' },
  { name: 'About' },
  { name: 'Projects' },
  { name: 'Contact' },
])

const navitemClick = () => {
    this.$refs.targetRef.scrollIntoView({ behavior: 'smooth' });
}

</script>

<template>
    <ul class="">
        <a :href="`#${nav.name}`" v-for="nav in navitems" :key="nav" 
                class="navitem flex justify-center items-center cursor-pointer group">
            <li>
                <div class="relative  py-3 md:py-2 text-md cursor-pointer font-[600]">
                    {{ nav.name }}
                    <span class="underline absolute bottom-0 left-[50%] translate-x-[-50%] block h-[2px] bg-black duration-200 w-0 group-hover:w-full dark:bg-[#fff]"></span>
                </div>
            </li>
        </a>
        <button class="toggleDark" @click="toggleDark()" v-if="isDark">
            <i class="fa-solid fa-sun text-2xl"></i>
        </button>
        <button class="toggleDark" @click="toggleDark()" v-else>
            <i class="fa-solid fa-moon text-2xl"></i>
        </button>
    </ul>
</template>