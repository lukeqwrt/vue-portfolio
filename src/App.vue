<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/header/Header.vue'

</script>

<template>
  <div class="main dark:!bg-[#121212]">
    <!-- header -->
    <Header />

    <!-- main -->
    <RouterView />
  </div>
</template>

<style>
html.dark,
.main{
  color-scheme: dark;
  
}
</style>