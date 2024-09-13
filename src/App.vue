<template>
  <div class="main-container">
   <HomePage />
   <SecondPage/>
 </div>
</template>

<script>
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';
import './Style/app.css'
import 'bootstrap-icons/font/bootstrap-icons.css';  // Import Bootstrap CSS
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
export default {
  name: 'App',
  components: {
    HomePage,
    SecondPage,
    // // ThirdPage
  },
  mounted(){
    gsap.registerPlugin(ScrollTrigger)
    // gsap.to("#second-container", {
    //   scrollTrigger: {
    //     trigger: "#first-container", // Trigger when the HomePage comes into view
    //     start: "top top", // Start the animation when the top of HomePage hits the top of the viewport
    //     // end: "bottom top", // End the animation when the bottom of HomePage hits the top of the viewport
    //     scrub: true, // Smooth animation linked to scroll position
    //     pin: "#first-container", // Pin the HomePage while the SecondPage scrolls over it
    //   },
    //   y: "-70%", // Move the SecondPage up over HomePage
    //   ease: "none", // Linear easing to smoothly stack
    // });
  }
}
</script>
<style>
  
</style>