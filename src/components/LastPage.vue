<template>
  <div class="last-page-container">
    <div class="contact-title">Contact</div>
    <div class="resume" id="common">Download my resume <a :href="resume" download>Here</a></div>
    <div class="social-media">
      <div class="social-title" id="common">You can also find me On</div>
      <div class="social-media-components">
        <span @click="openinstagram">
          <img :src="instagram" alt="" />
          <p>Instagram</p>
        </span>
        <span @click="openLinkedin">
          <img :src="linkedin" alt="" />
          <p>Linkedin</p>
        </span>
        <span @click="opengithub">
          <img :src="github" alt="" />
          <p>Github</p>
        </span>
        <span @click="openX">
          <img :src="twitterX" alt="" />
          <p>X</p>
        </span>
      </div>
      <div class="end-text">
        Hit me up on my Social Media <br />
        Lets create innovative Projects
      </div>
    </div>
  </div>
</template>

<script>
import instagram from "../assets/socialmeda/instagram.svg";
import twitterX from "../assets/socialmeda/twitter-x.svg";
import linkedin from "../assets/socialmeda/linkedin-icon-2.svg";
import github from "../assets/socialmeda/github.svg";
import resume from '../assets/resume/Sandeep Sreekumar.pdf'
import "../Style/lastpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      instagram: instagram,
      twitterX: twitterX,
      linkedin: linkedin,
      github: github,
      resume:resume
    };
  },
  methods: {
    openinstagram() {
      window.open("https://www.instagram.com/_.the.___.one._/", "_blank");
    },
    openLinkedin() {
      window.open(
        "https://www.linkedin.com/in/sandeep-sreekumar4067",
        "_blank"
      );
    },
    openX() {
      window.open("https://x.com/sandeep77368", "_blank");
    },
    opengithub() {
      window.open("https://github.com/sandeepsreekumar4067", "_blank");
    },
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    gsap.from(".contact-title", {
      scrollTrigger: {
        trigger: ".contact-title",
        start: "top 50%",
      },
      y: -100,
      opacity: 0,
      ease: "bounce.out",
      duration: 1.2,
    });
    gsap.from("#common", {
      scrollTrigger: {
        trigger: "#common",
        start: "top 50%",
      },
      y: 100,
      opacity: 0,
      stagger: 0.3,
      duration: 1.2,
    });
    gsap.from(".social-media-components span", {
      scrollTrigger: {
        trigger: ".social-media-components",
        start: "top 50%",
      },
      delay: 1,
      scale: 0,
      stagger: 0.4,
      ease: "bounce.out",
      duration: 1,
    });
    gsap.from(".end-text", {
      scrollTrigger: {
        trigger: ".end-text",
        start: "top 90%",
      },
      x: 100,
      opacity: 0,
      duration: 0.9,
    });
  },
};
</script>

<style>
</style>