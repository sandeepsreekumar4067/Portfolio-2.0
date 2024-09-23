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
        <div class="project-components">
          <span id="id1"></span>
          <span id="id2"></span>
          <span id="id3"></span>
          <span id="id4"></span>
          <span id="id5"></span>
          <span id="id6"></span>
          <span id="id7"></span>
          <span id="id8"></span>
        </div>
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
        endTrigger: "#fmain",
        end: "bottom bottom",
      },
    });
    tl.from(".fourth-page-title", {
      x: -100,
      opacity: 0,
    });
    tl.from(".project-components", {
      yPercent: 100,
      duration: 1.5,
    });
    tl.from('.project-components span',{
      scale:0,
      ease:'circ.inOut',
      stagger:0.2
    })
  },
};
</script>

<style>
</style>