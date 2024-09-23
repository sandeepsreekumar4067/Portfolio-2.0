<template>
  <div class="fourth-wrapper" id="fmain">
    <div class="fourth-page-container" id="fcomp">
      <div class="background-image">
        <img :src="mountainImage" alt="" />
      </div>
      <div class="fourth-page-components">
        <div class="fourth-page-title">
          <span>Projects</span>
        </div>
        <div class="project-components"></div>
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/fourthpage.css";
import mountainImage from "../assets/background/mountainImage.jpg";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      mountainImage: mountainImage,
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: "#fcomp",
        start: "top top",
        pin: true,
        endTrigger:'#fmain',
        end: "bottom bottom",
        scrub: 1,
      },
    });
    tl.from(".fourth-page-title", {
      x:-100,
      opacity:0
    });
  },
};
</script>

<style>
</style>