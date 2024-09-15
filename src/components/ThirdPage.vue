<template>
  <div class="third-page-container" id="tmain">
    <div class="third-page-components" id="components">
      <div class="circle">My Skills</div>
      <div class="skill-container"></div>
    </div>
  </div>
</template>

<script>
import "../Style/thirdpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    const timeline = gsap.timeline({
      scrollTrigger: {
        trigger: "#components",
        markers: true,
        start: "top 10%",
        pin: true,
        scrub: 1,
        endTrigger: "#tmain",
        end: "bottom bottom",
      },
    });
    timeline.from(".circle", {
      opacity: 0,
      scale: 0,
    });
  },
};
</script>

