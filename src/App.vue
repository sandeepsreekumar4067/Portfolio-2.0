<template>
  <HomePage />
  <SecondPage />
  <ThirdPage />
</template>

<script>
import HomePage from "./components/HomePage.vue";
import SecondPage from "./components/SecondPage.vue";
import ThirdPage from "./components/ThirdPage.vue";
import "./Style/app.css";
import "bootstrap-icons/font/bootstrap-icons.css"; // Import Bootstrap CSS
import {gsap} from 'gsap'
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  name: "App",
  components: {
    HomePage,
    SecondPage,
    ThirdPage,
  },
  mounted(){
    gsap.registerPlugin(ScrollTrigger)
    gsap.utils.toArray('.panel').forEach((panel)=>{
      ScrollTrigger.create({
        trigger:panel,
        start:'top top',
        pin:true,
      })
  })
  }
};
</script>
<style>
</style>