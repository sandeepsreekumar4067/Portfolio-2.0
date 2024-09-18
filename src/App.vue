<template>
  <HomePage />
  <SecondPage />
  <ThirdPage />
  <FourthPage/>
</template>

<script>
import FourthPage from './components/FourthPage.vue';
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';
import ThirdPage from './components/ThirdPage.vue';
import './Style/app.css'
import 'bootstrap-icons/font/bootstrap-icons.css';  // Import Bootstrap CSS
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
export default {
  name: "App",
  components: {
    HomePage,
    SecondPage,
    ThirdPage,
    FourthPage
  },
  mounted(){
    gsap.registerPlugin(ScrollTrigger)
    const panels = gsap.utils.toArray('.panel')
    panels.forEach((panel)=>{
      ScrollTrigger.create({
        trigger:panel,
        start:'top top',
        pin:true,
        pinSpacing:false,
        snap:1
      })
    })
  }
};
</script>
<style>
</style>