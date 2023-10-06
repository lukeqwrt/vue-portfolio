<script setup>
import { ref } from 'vue'
import MobileNav from '../header/MobileNav.vue';
import NavItems from '../header/NavItems.vue';


// navbar toggle click event
const toggleActive = ref(false)
const navBarClicked = () => {
  toggleActive.value = !toggleActive.value
}

</script>

<template>
  <header class=" h-[75px] w-full px-5 md:px-12 lg:container lg:mx-auto lg:h-[100px]">
      <nav class="h-full flex items-center justify-between relative">
        <h3 class="logo text-lg sm:text-xl font-[600] lg:text-2xl">Luke&Aira</h3>

        <div @click="navBarClicked()" class="navbar-toggle absolute right-0 top-[50%] translate-y-[-50%] cursor-pointer block md:hidden z-20">
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black duration-200" :class="toggleActive ? 'translate-y-[8px] rotate-[45deg]' : 'translate-y-[0px]' "></span>
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black duration-200" :class="toggleActive ? 'opacity-0' : 'opacity-1' "></span>
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black duration-200" :class="toggleActive ? 'translate-y-[-8px] rotate-[-45deg]' : 'translate-y-[0px]' "></span>
        </div>

        <NavItems class="nav-items hidden md:flex gap-6 items-center" />

        <MobileNav :toggleActive="toggleActive" />
      </nav>
  </header>
</template>