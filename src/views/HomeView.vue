<script setup>
import TitleContentVue from "../components/landing/TitleContent.vue";
import White from '../assets/mypic/white.jpg'
import TechStack from '../components/landing/TechStack.vue'

</script>

<template>
  <main>
    <div class="landing p-5 md:p-12 container mx-auto flex flex-col justify-start sm:justify-center items-center relative" style="height: calc(100vh - 75px);">
      <div class="wrapper">
        <div class="flex-1 flex gap-4 flex-col justify-center items-center sm:items-start sm:flex-row-reverse sm:gap-10 sm:flex-[unset] sm:mb-[4rem] md:mb-[6rem] md:gap-[3rem] ">
          <img :src="White" alt="" class="rounded-full object-cover h-auto w-[180px] sm:w-[200px] md:w-[240px]">
          <!-- title content -->
          <TitleContentVue />
        </div>
        <TechStack />
      </div>
    </div>
  </main>
</template>
