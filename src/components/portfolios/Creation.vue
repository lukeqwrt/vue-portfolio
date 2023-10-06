<script setup>
const props = defineProps(['PortDetails'])

const { name, image, details, tools, code, livedemo } = props.PortDetails
</script>

<template>
    <div class="detail_image mb-5 px-5">
        <img :src="image" alt="none" class="rounded-md h-auto sm:max-w-[320px] lg:max-w-[400px]">
    </div>
    <div class="detail_content px-3 text-center">
        <h2 class="font-bold text-lg mb-2">{{ name }}</h2>
        
        <p class="text-[#686868] text-sm mb-5">{{ details }}</p>

        <ul class="tool_use flex justify-center gap-5 mb-6">
            <li class="font-bold" v-for="tool in tools" :key="tool">
                {{ tool }}
            </li>
        </ul>
        <div class="links flex justify-around mt-5 text-md font-bold">
            <a href="" class="flex gap-3 justify-center items-center">
                <span>Code</span>
                <img class="h-[25px] w-[25px]" src="../../assets/img/github-mark.png" alt="">
            </a>
            <a href="" class="flex gap-3 justify-center items-center">
                <span>Live Demo</span>
                <i class="fa-solid fa-arrow-up-right-from-square"></i>
            </a>
        </div>
    </div>
</template>