<template>
  <div class="homepage-container" >
    <div class="wrapper">
      <div class="left-container">
        <div class="left-about-container">
          <div class="left-title" id="name">Hi I'm</div>
          <div>
            <div class="left-name" id="name">Sandeep Sreekumar</div>
            <div class="left-desc" id="name">Frontend Developer / Full Stack</div>
          </div>
        </div>
        <div class="left-button-container">
          <span id="init-button">
            <i class="bi bi-github"></i>
          </span>
          <span id="button">
            <i class="bi bi-linkedin"></i>
          </span>
          <span id="button">
            <i class="bi bi-instagram"></i>
          </span>
          <span id="button">
            <i class="bi bi-twitter-x"></i>
          </span>
        </div>
      </div>
      <div class="right-container">
        <img :src="homeImage" alt="" id="home-img" />
      </div>
    </div>

  </div>
</template>

<script>
import "../Style/homepage.css";
import homeImage from "../assets/homeImage2.png";
import { gsap } from "gsap";
export default {
  data() {
    return {
      homeImage: homeImage,
    };
  },
  mounted(){

    gsap.from('#home-img',{
      duration:1.8,
      x:'50%',
      opacity:0,
    })
    gsap.from('#name',{
      duration:1,
      y:200,
      stagger:0.4,
      opacity:0
    })
    gsap.from('#init-button',{
      duration:1.5,
      opacity:0,
      display:'none'
    })
    gsap.from('#button',{
      duration:1,
      opacity:0,
      stagger:0.3,
      x:-100,
      delay:0.2
    })
  }
};
</script>
