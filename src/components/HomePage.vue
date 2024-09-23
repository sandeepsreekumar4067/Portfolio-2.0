<template>
  <div class="home-wrapper">
    <div class="homepage-container">
      <div class="wrapper">
        <div class="left-container">
          <div class="left-about-container">
            <div class="left-title" id="name">Hi I'm</div>
            <div>
              <div class="left-name" id="name">Sandeep Sreekumar</div>
              <div class="left-desc" id="name">
                Frontend Developer / Full Stack
              </div>
            </div>
          </div>
          <div class="left-button-container">
            <span id="init-button" @click="openinstagram" >
              <img :src="instagram" alt="" >
            </span>
            <span id="button" class="button1" @click="openLinkedin">
              <img :src="linkedin" alt="" />
            </span>
            <span id="button" class="button2" @click="opengithub">
              <img :src="github" alt="" />
            </span>
            <span id="button" class="button3" @click="openX">
              <img :src="twitterX" alt="" />
            </span>
          </div>
        </div>
        <div class="right-container">
          <img :src="homeImage" alt="" id="home-img" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/homepage.css";
import instagram from "../assets/socialmeda/instagram.svg";
import twitterX from "../assets/socialmeda/twitter-x.svg";
import linkedin from "../assets/socialmeda/linkedin-icon-2.svg";
import github from "../assets/socialmeda/github.svg";
import homeImage from "../assets/homeImage2.png";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      homeImage: homeImage,
      instagram: instagram,
      twitterX: twitterX,
      linkedin: linkedin,
      github: github,
    };
  },
  methods:{
    openinstagram(){
      window.open('https://www.instagram.com/_.the.___.one._/','_blank')
    },
    openLinkedin(){
      window.open('https://www.linkedin.com/in/sandeep-sreekumar4067','_blank')
    },
    openX(){
      window.open('https://x.com/sandeep77368','_blank')
    },
    opengithub(){
      window.open('https://github.com/sandeepsreekumar4067','_blank')
    }
  },

  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: ".home-wrapper",
        start: "top top",
        scrub: 1,
        pin: true,
      },
    });
    tl.to("#name", {
      x: "-130%",
      stagger: 0.4,
    });
    tl.to("#init-button", {
      scale: 0,
    });
    tl.to(".button1", {
      scale: 0,
    });
    tl.to(".button2", {
      scale: 0,
    });
    tl.to(".button3", {
      scale: 0,
    });
    tl.to("#home-img", {
      scale: 2,
      opacity: 0,
    });
    tl.to("left-container", {
      display: "none",
    });
    gsap.from("#home-img", {
      duration: 1.8,
      x: "50%",
    });
    gsap.from("#name", {
      duration: 1,
      y: 200,
      stagger: 0.4,
      opacity: 0,
    });
    gsap.from("#init-button", {
      duration: 1.5,
      opacity: 0,
      display: "none",
    });
    gsap.from("#button", {
      duration: 1,
      opacity: 0,
      stagger: 0.3,
      x: -100,
      delay: 0.2,
    });
  },
};
</script>
