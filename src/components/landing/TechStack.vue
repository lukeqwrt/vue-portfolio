<script setup>
import { ref } from 'vue'
import html from '../../assets/skills/html.png'
import css from '../../assets/skills/css.png'
import js from '../../assets/skills/js.png'
import tailwind from '../../assets/skills/tailwind.png'
import bootstrap from '../../assets/skills/bootstrap.png'
import sass from '../../assets/skills/sass.png'
import firebase from '../../assets/skills/firebase.png'
import vue from '../../assets/skills/vuejs.png'

const techStack = ref([html, css, js, tailwind, bootstrap, sass, firebase ,vue])

</script>

<template>
    <div class="tech pe-2 flex gap-4 absolute bottom-0 left-0 sm:left-0  md:left-0 md:bottom-0 md:gap-11">
        <div class="w-[60px] flex gap-3 md:gap-5 justify-between items-center">
            <span class="font-bold text-sm md:whitespace-nowrap lg:text-lg ">Tech Stack </span>
            <div class=" font-[400] block">|</div> 
        </div>
        <ul class="tech-logo ms-2 flex items-center flex-wrap gap-5 md:gap-7 md:ms-5 lg:ms-10 lg:gap-11">
            <li v-for="skill in techStack" :key="skill">
                <img :src="skill" class="h-[20px] w-[20px] md:h-[25px] md:w-[25px] lg:h-[30px] lg:w-[30px]">
            </li>
        </ul>
    </div>
</template>