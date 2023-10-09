<script setup>
import TitleContentVue from "../components/landing/TitleContent.vue"
import White from '../assets/mypic/white.jpg'
import TechStack from '../components/landing/TechStack.vue'
import AboutMe from "../components/about/AboutMe.vue"
import Portfolio from "../components/portfolios/Portfolio.vue"
import Contact from "../components/contact/Contact.vue"
import Footer from "../components/footer/footer.vue"
import svg from "../assets/img/me6.png"
</script>

<template>
  <main>
    <!-- landing -->
    <section id="Home" class="landing h-[100vh] p-5 md:p-12 container mx-auto flex flex-col justify-center sm:justify-center items-center " >
      <div class="wrapper w-full sm:w-[unset] h-full lg:max-h-[580px] flex flex-col justify-center items-center relative">
        <div class="flex-1 flex gap-4 flex-col justify-center items-center sm:items-start sm:flex-row-reverse sm:gap-10 sm:flex-[unset]  md:items-center  md:gap-[3rem] lg:gap-[9rem] ">
          <!-- <img :src="White" alt="" class="rounded-full object-cover h-auto w-[180px] sm:w-[200px] md:w-[290px]"> -->
          <img :src="svg" alt="" class="object-cover h-auto w-[180px] sm:w-[200px] md:w-[290px]" style="clip-path: url('../assets/mypic/white.jpg');">
          <!-- title content -->
          <TitleContentVue />
        </div>
        <TechStack />
      </div>
    </section>

    <!-- about me -->
    <AboutMe />

    <!-- Portfolios -->
    <Portfolio />

    <!-- Contact -->
    <Contact />

    <!-- Footer -->
    <Footer />
  </main>
</template>

<style scoped>
  /* .landing{
    height: calc(100vh - 75px);
  }

  @media screen and (min-width: 1024px) {
    .landing{
      height: calc(100vh - 100px);
    }
} */
</style>
