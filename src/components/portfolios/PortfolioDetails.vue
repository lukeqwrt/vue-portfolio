<script setup>
import { ref } from 'vue'
import CreationVue from './Creation.vue'
import coffee from '../../assets/projects-img/coffee.png'
import disney from '../../assetS/projects-img/disney2.png'
import store from '../../assetS/projects-img/Capture.jpg'
import hxh from '../../assetS/projects-img/hunterxhunterpage.jpg'
import todo from '../../assetS/projects-img/todo-proj.jpg'

const portfolios = ref([
    { name: 'Coffee Website', image:coffee, details:'A coffee website is a website that allow the user to view and choose their favorite coffee in the menu', tools:['HTML', 'CSS', 'JavaScript'], code:'https://github.com/lukeqwrt/Coffee-shop', livedemo:'https://coffee-shop-sillano.netlify.app/' },
    { name: 'Disney Clone', image:disney, details:'A Disney Plus Clone using tmdb api and Firebase Authentication enabling the user to view trending movies by genre and also see the details.', tools:['Vue JS', 'SCSS'], code:'https://github.com/lukeqwrt/disney-clone', livedemo:'https://lukeqwrt.github.io/disney-clone/' },
    { name: 'E-commerce Website', image:store, details:'This is and E-commerce website store that allow the user to shop and pick items to add cart and has a nice design and page', tools:['HTML', 'CSS', 'JavaScript'], code:'https://github.com/lukeqwrt/store-website', livedemo:'https://lukeqwrt.github.io/store-website/' },
    { name: 'Anime Website', image:hxh, details:'This is a simple anime website that shows the details of the authors and where we can watch it etc.', tools:['HTML', 'CSS', 'JavaScript'], code:'https://github.com/lukeqwrt/HunterXHunter', livedemo:'https://hunterxhunterpage.netlify.app/' },
    { name: 'Todo App', image:todo, details:'This is a simple todo-list web application to practice my skills in vue.', tools:['Vue JS', 'CSS'], code:'https://github.com/lukeqwrt/TODO', livedemo:'https://lukeqwrt.github.io/TODO/' },
])

</script>

<template>
    <ul class="portfolio_details grid gap-16 py-5 ">
        <li 
            :class="{'sm:flex-row-reverse' : index % 2 == 0}"
            class="dev md:flex sm:gap-5 lg:gap-10 p-5" v-for="(portfolio, index) in portfolios" :key="portfolio"
        >
            <CreationVue :PortDetails="portfolio" />
        </li>
    </ul>
</template>