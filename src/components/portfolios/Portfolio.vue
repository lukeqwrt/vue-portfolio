<script setup>
import PortfolioDetails from './PortfolioDetails.vue';

</script>

<template>
   <section class="portfolio py-5">
    <div class="portfolio_wrapper container lg:py-12 sm:max-w-[566px] md:max-w-[720px] lg:max-w-[840px] mx-auto">
        <div class="portfolio_title mb-12">
            <h3 class="section_title">PORTFOLIO</h3>
            <h1 class="second_title">Each project is a unique piece of development</h1>
        </div>
        
        <PortfolioDetails />
    </div>
   </section>
</template>