<script setup>
import { ref } from 'vue'
import html from '../../assets/skills/html.png'
import css from '../../assets/skills/css.png'
import js from '../../assets/skills/js.png'
import tailwind from '../../assets/skills/tailwind.png'
import bootstrap from '../../assets/skills/bootstrap.png'
import sass from '../../assets/skills/sass.png'
import firebase from '../../assets/skills/firebase.png'

const techStack = ref([html, css, js, tailwind, bootstrap, sass, firebase])

</script>

<template>
    <div class="tech pe-2 flex gap-2 absolute bottom-5 left-5 sm:relative sm:left-0 lg:gap-4">
        <div class="w-[60px] sm:w-[100px] lg:w-[120px] flex justify-between items-center">
            <span class="font-bold text-sm lg:text-lg">Tech Stack </span>
            <div class=" font-[400]">|</div> 
        </div>
        <ul class="tech-logo ms-2 flex items-center flex-wrap gap-5 lg:gap-11">
            <li v-for="skill in techStack" :key="skill">
                <img :src="skill" class="h-[20px] w-[20px] md:h-[25px] md:w-[25px] lg:h-[30px] lg:w-[30px]">
            </li>
        </ul>
    </div>
</template>