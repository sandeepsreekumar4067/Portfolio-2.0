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
          <span id="id1">
            <img :src="projectimg" alt="">
          </span>
          <span id="id2">
            <img :src="projectimg" alt="">
          </span>
          <span id="id3">
            <img :src="projectimg" alt="">
          </span>
          <span id="id4">
            <img :src="projectimg" alt="">
          </span>
          <span id="id5">
            <img :src="projectimg" alt="">
          </span>
          <span id="id6">
            <img :src="projectimg" alt="">
          </span>
          <span id="id7">
            <img :src="projectimg" alt="">
          </span>
          <span id="id8">
            <img :src="projectimg" alt="">
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/fourthpage.css";
import mountainImage from "../assets/background/mountainImage.jpg";
import projectimg from '../assets/project images/img1 (1).jpg'
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      mountainImage: mountainImage,
      projectimg:projectimg
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