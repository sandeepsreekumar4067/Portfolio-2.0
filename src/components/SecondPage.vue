<template>
  <div class="secondPage-container" id="sc-main">
    <div class="secondPage-display-container" id="sc-display">
      <div class="secondPage-circle-container" id="sc-circle"></div>
    </div>
  </div>
</template>

<script>
import "../Style/secondpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    gsap.to("#sc-circle", {
      y: "34rem", // Moves the circle down 20rem
      ease: "bounce.out", // Bounce effect on fall
      duration: 2, // Total time for the fall and bounce
      scrollTrigger: {
        trigger: "#sc-main", // When the top of secondPage-container hits the top of the viewport
        start: "top 10%", // Start when the top of sc-main hits the top of the viewport
        toggleActions: "play none none none", // Only play once
      },
    });
  },
};
</script>

<style>
</style>