<template>
  <div class="third-page-container" id="tmain">
    <div class="third-page-components" id="components">
      <div class="circle">My Skills</div>
      <div class="skill-container">

      </div>
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
        toggleActions: 'play reverse play reverse', // Ensures the animation reverses when scrolling back up
      },
    });
    timeline.from(".circle", {
      opacity: 0,
      x:-300
    });
    timeline.from('.skill-container',{
      width:'2rem',
      height:'2rem',
      opacity:0,    
      snap:1
    })
  },
};
</script>

