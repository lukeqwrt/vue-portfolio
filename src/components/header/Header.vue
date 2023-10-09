<script setup>
import { ref, onMounted } from 'vue'
import MobileNav from '../header/MobileNav.vue';
import NavItems from '../header/NavItems.vue';


// navbar toggle click event
const toggleActive = ref(false)
const navBarClicked = () => {
  toggleActive.value = !toggleActive.value
}

const currentwidth = ref() 
 


  window.addEventListener("resize", () => {
    if(currentwidth.value <= 768){
        toggleActive.value = false;
        return;
    }
    toggleActive.value = false
    return
  })
  

</script>

<template>
  <header class="header bg-white dark:bg-[#121212] h-[75px]   md:px-12  lg:h-[78px] fixed w-full z-50 top-0 left-0 right-0">
      <nav class="h-full  flex items-center justify-between relative px-5 lg:container lg:mx-auto">
        <h3 class="logo text-lg sm:text-xl font-[600] lg:text-1xl">Luke.dev();</h3>
        <div @click="navBarClicked()" class="navbar-toggle absolute right-5 top-[50%] translate-y-[-50%] cursor-pointer block md:hidden z-20">
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black dark:bg-white duration-200" :class="toggleActive ? 'translate-y-[8px] rotate-[45deg]' : 'translate-y-[0px]' "></span>
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black dark:bg-white duration-200" :class="toggleActive ? 'opacity-0' : 'opacity-1' "></span>
          <span class="w-[25px] h-[3px] my-[5px] mx-auto block bg-black dark:bg-white duration-200" :class="toggleActive ? 'translate-y-[-8px] rotate-[-45deg]' : 'translate-y-[0px]' "></span>
        </div>

        <NavItems class="nav-items hidden md:flex gap-6 items-center" />

        <MobileNav :toggleActive="toggleActive" />
      </nav>
  </header>
</template>

<style>
html.dark .header{
  /* box-shadow: rgba(255, 255, 255, 0.15) 0px 5px 15px 0px; */
}
</style>