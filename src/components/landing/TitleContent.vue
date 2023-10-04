<script setup>
import hand from '../../assets/img/hand.png'
import github from '../../assets/img/github-mark.png'
import linkedin from '../../assets/img/linkedin.png'
</script>

<template>
    <div class="content_wrapper justify-self-center grid w-full gap-4"> 
        <div class="title-content justify-self-center w-[201px] md:w-[340px]  relative">
            <h1 class="text-3xl md:text-5xl font-bold ">
                Jr. Front-End Developer 
            </h1>
            <img :src="hand" alt="asas" class="w-[30px] md:w-[40px] h-auto absolute right-[0%] md:right-[10%] bottom-1">
        </div>

        <div class="details w-full max-w-[255px] text-center sm:text-left md:w-full md:max-w-[310px] justify-self-center md:justify-self-start">
            <span class="text-[13px] md:text-[14px]">Hi, I'm Luke Adrian Sillano. A passionate front Front-End Developer blablabla</span>
        </div>

        <div class="logos justify-self-center sm:justify-self-start flex items-center gap-3 justify-center">
            <img :src="github" alt="asd" class="h-auto w-[20px]">
            <img :src="linkedin" alt="asd" class="h-auto w-[20px]">
        </div>
    </div>
</template>