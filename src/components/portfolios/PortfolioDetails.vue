<script setup>
import { ref } from 'vue'
import CreationVue from './Creation.vue'
import coffee from '../../assets/projects-img/coffee.png'

const portfolios = ref([
    { name: 'Coffee Website', image:coffee, details:'A coffee website is a website that allow the user to view and choose their favorite coffee in the menu', tools:['HTML', 'CSS', 'JavaScript'], code:'https://github.com/lukeqwrt/Coffee-shop', livedemo:'https://coffee-shop-sillano.netlify.app/' }
])

</script>

<template>
    <ul class="portfolio_details py-5">
        <li class="dev sm:flex sm:gap-5 lg:gap-8" v-for="portfolio in portfolios" :key="portfolio">
            <CreationVue :PortDetails="portfolio" />
        </li>
    </ul>
</template>