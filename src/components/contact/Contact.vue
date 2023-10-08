<script setup>
import { ref } from 'vue'

const contact_details = ref([
    { name: 'Location', description: 'Philippines', image:'fa-solid fa-map-location-dot'},
    { name: 'Email', description: 'lukeadrian9@gmail.com', image:'fa-solid fa-square-envelope'},
    { name: 'Facebook', description: 'luke sillano', image:'fa-brands fa-square-facebook'},
])
</script>

<template>
    <section id="Contact" class="contact py-12 my-5">
        <div class="contact_wrapper lg:py-12 container sm:max-w-[566px] md:max-w-[720px] lg:max-w-[840px] mx-auto flex flex-col ">
            <div class="contact-title mb-5 md:mb-10">
                <h3 class="section_title">CONTACT ME</h3>
                <h1 class="second_title">Don't be shy! Message me!</h1>
            </div>
            <div class="contact_details flex flex-wrap justify-between md:justify-start gap-8 py-4 md:gap-12">
                <div class="detail flex-grow-1 flex items-center gap-4 md:gap-5" v-for="cd in contact_details" :key="cd.name">
                    <i :class="cd.image" class=" text-2xl md:text-4xl text-[#478ae2]"></i>
                    <div class="detail_content flex gap-1 flex-col">
                        <span class="font-bold text-md">{{ cd.name }}</span>
                        <span class="text-[#686868] text-sm">{{ cd.description }}</span>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>