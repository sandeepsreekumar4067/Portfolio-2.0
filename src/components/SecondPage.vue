<template>
  <div class="secondPage-container" >
    <span id="sc1">
      Hi, I'm Sandeep Sreekumar I'm a Full Stack Developer with a focus on web
      and mobile applications.
    </span>
    <span id="sc2">
      I specialize in Frontend Development using HTML, CSS, JavaScript, React,
      and Vue.js
    </span>
    <span id="sc3">
      I specialize in Frontend Development using HTML, CSS, JavaScript, React,
      and Vue.js,
    </span>
    <span id="sc4">
        Currently, I'm pursuing a B.Tech in Computer Science and Engineering at VJCET.
    </span>
    <span id="sc5">
        I'm passionate about building intuitive and impactful digital solutions
    </span>
  </div>
</template>

<script>
import "../Style/secondpage.css";
import {gsap} from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger';
export default {
    data(){
        return{

        }
    },
    mounted(){
        gsap.registerPlugin(ScrollTrigger);
    }
};
</script>

<style>
</style>