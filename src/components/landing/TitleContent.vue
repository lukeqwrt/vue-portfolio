<script setup>
import hand from '../../assets/img/hand.png'
import githubblack from '../../assets/img/github-mark.png'
import githubwhite from '../../assets/img/github-mark-white.png'
import linkedin from '../../assets/img/linkedin.png'
import { computed } from 'vue'
import { useDark } from "@vueuse/core"

const isDark = useDark()

</script>

<template>
    <div class="content_wrapper justify-self-center grid w-full gap-4 lg:gap-7"> 
        <div class="title-content justify-self-center sm:justify-self-start w-[201px] md:w-[340px]  relative">
            <h1 class="text-3xl md:text-5xl font-bold ">
                 Front-End Developer 
            </h1>
            <img :src="hand" alt="asas" class="w-[30px] md:w-[40px] h-auto absolute right-[0%] md:right-[10%] bottom-1">
        </div>

        <div class="details w-full max-w-[255px] text-center sm:text-left md:w-full md:max-w-[310px] justify-self-center md:justify-self-start">
            <span class="text-[13px] md:text-[14px]">Hi, I'm Luke Adrian Sillano. A passionate Front-End Developer. Let's make something special.</span>
        </div>

        <div class="logos justify-self-center sm:justify-self-start flex items-center gap-3 md:gap-5 justify-center">
            <a href="https://github.com/lukeqwrt">
                <div v-if="isDark">
                    <img :src="githubwhite" alt="asd" class="h-auto w-[20px] lg:w-[28px]">
                </div>
                <div v-else>
                    <img :src="githubblack" alt="asd" class="h-auto w-[20px] lg:w-[28px]">
                </div>
            </a>
            <a href="https://www.linkedin.com/in/luke-adrian-sillano-a404201a0">
                <img :src="linkedin" alt="asd" class="h-auto w-[20px] lg:w-[28px]">
            </a>
        </div>
    </div>
</template>