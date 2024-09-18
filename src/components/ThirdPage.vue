<template>
  <div class="third-page-container" id="tmain">
    <div class="third-page-components" id="components">
      <div class="skill-title">My Skills</div>
      <div class="skill-container1">
        <div class="row row1">
          <div class="row-title row-title-1">Programming Languages</div>
          <div class="skill-component skill-component-1">
            <span
              v-for="(languageIcon, key) in pl"
              :key="key"
              class="skill-images-1"
            >
              <img :src="languageIcon" alt="" />
            </span>
          </div>
        </div>
      </div>
      <div class="skill-container2">
        <div class="row row2">
          <div class="row-title row-title-2">Web Development</div>
          <div class="skill-component skill-component-2">
            <span
              v-for="(languageIcon, key) in wd"
              :key="key"
              class="skill-images-2"
            >
              <img :src="languageIcon" alt="" />
            </span>
          </div>
        </div>
      </div>
      <div class="skill-container3">
        <div class="row row3">
          <div class="row-title row-title-3">Mobile App Development</div>
          <div class="skill-component skill-component-3">
            <span
              v-for="(languageIcon, key) in md"
              :key="key"
              class="skill-images-3"
            >
              <img :src="languageIcon" alt="" />
            </span>
          </div>
        </div>
      </div>
      <div class="skill-container3">
        <div class="row row4">
          <div class="row-title row-title-4">Databases</div>
          <div class="skill-component skill-component-4">
            <span
              v-for="(languageIcon, key) in db"
              :key="key"
              class="skill-images-4"
            >
              <img :src="languageIcon" alt="" />
            </span>
          </div>
        </div>
      </div> 
    </div>
  </div>
</template>

<script>
import "../Style/thirdpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import c from "../assets/languageIcons/c.png";
import cpp from "../assets/languageIcons/c++.png";
import python from "../assets/languageIcons/python.png";
import java from "../assets/languageIcons/java.png";
import js from "../assets/languageIcons/js.png";
import dart from "../assets/languageIcons/dart.png";
import experss from "../assets/languageIcons/expressjs.png";
import vue from "../assets/languageIcons/vueJs.png";
import firebase from "../assets/languageIcons/fireabase.png";
import flutter from "../assets/languageIcons/flutter.png";
import react from "../assets/languageIcons/react.png";
import node from "../assets/languageIcons/nodejs.png";
import mongo from "../assets/languageIcons/mongoDb.png";
import spline from "../assets/languageIcons/spline.png";
import ts from "../assets/languageIcons/typescript.png";
import mySql from "../assets/languageIcons/mySql.png";
import html from "../assets/languageIcons/html.png";
import css from "../assets/languageIcons/css.png";
import github from "../assets/languageIcons/github.png";

export default {
  data() {
    return {
      c: c,
      cpp: cpp,
      python: python,
      java: java,
      js: js,
      dart: dart,
      experss: experss,
      vue: vue,
      firebase: firebase,
      flutter: flutter,
      react: react,
      node: node,
      mongo: mongo,
      spline: spline,
      ts: ts,
      mySql: mySql,
      html: html,
      css: css,
      github: github,
      pl: [c, cpp, python, java, js],
      wd: [html, css, react, vue, node, experss],
      md: [flutter],
      db: [firebase, mySql, mongo],
      tools: [github],
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);


    //for Programming Languages

    gsap.from(".skill-title", {
      scrollTrigger: {
        trigger: ".skill-title",
        start: "top 90%",
        scrub: 1,
        end: "top 50%",
      },
      x: -500,
      opacity: 0,
    });

    gsap.from(".row-title-1", {
      scrollTrigger: {
        trigger: ".row-title-1",
        start: "top 70%",
        scrub: 1,
        end: "top 50%",
      },
      x: -300,
      opacity: 0,
    });
    gsap.from(".skill-images-1", {
      scrollTrigger: {
        trigger: ".skill-component-1", // The container for the images
        start: "top 60%", // When to start the animation
        end: "top 50%", // When to end the animation
        scrub: 1, // Smooth scrolling
      },
      scale: 0, // Start with scale 0
      opacity: 0, // Start with opacity 0
      stagger: 0.2, // Delay between each image's animation
      ease: "back.out(1.7)", // Ease effect
    });
    gsap.to('.skill-title-1',{
      scrollTrigger:{
        trigger:'.skill-container1',
        start:'bottom 80%',
        scrub:1,
        end:'bottom 60%'
      },
      x:-300,
      opacity:0
    })

    //for Web development

    gsap.from(".row-title-2", {
      scrollTrigger: {
        trigger: ".row-title-2",
        start: "top 70%",
        scrub: 1,
        end: "top 50%",
      },
      x: -300,
      opacity: 0,
    });
    gsap.from(".skill-images-2", {
      scrollTrigger: {
        trigger: ".skill-component-2", // The container for the images
        start: "top 60%", // When to start the animation
        end: "top 50%", // When to end the animation
        scrub: 1, // Smooth scrolling
      },
      scale: 0, // Start with scale 0
      opacity: 0, // Start with opacity 0
      stagger: 0.2, // Delay between each image's animation
      ease: "back.out(1.7)", // Ease effect
    });
    gsap.to('.skill-title-2',{
      scrollTrigger:{
        trigger:'.skill-container2',
        start:'bottom 80%',
        scrub:1,
        end:'bottom 60%'
      },
      x:-300,
      opacity:0
    })

    //for mobile development

    gsap.from(".row-title-3", {
      scrollTrigger: {
        trigger: ".row-title-3",
        start: "top 70%",
        scrub: 1,
        end: "top 50%",
      },
      x: -300,
      opacity: 0,
    });
    gsap.from(".skill-images-3", {
      scrollTrigger: {
        trigger: ".skill-component-3", // The container for the images
        start: "top 60%", // When to start the animation
        end: "top 50%", // When to end the animation
        scrub: 1, // Smooth scrolling
      },
      scale: 0, // Start with scale 0
      opacity: 0, // Start with opacity 0
      stagger: 0.2, // Delay between each image's animation
      ease: "back.out(1.7)", // Ease effect
    });
    gsap.to('.skill-title-3',{
      scrollTrigger:{
        trigger:'.skill-container3',
        start:'bottom 80%',
        scrub:1,
        end:'bottom 60%'
      },
      x:-300,
      opacity:0
    })

    //for database


    gsap.from(".row-title-4", {
      scrollTrigger: {
        trigger: ".row-title-4",
        start: "top 70%",
        scrub: 1,
        end: "top 50%",
      },
      x: -300,
      opacity: 0,
    });
    gsap.from(".skill-images-4", {
      scrollTrigger: {
        trigger: ".skill-component-4", // The container for the images
        start: "top 60%", // When to start the animation
        end: "top 50%", // When to end the animation
        scrub: 1, // Smooth scrolling
      },
      scale: 0, // Start with scale 0
      opacity: 0, // Start with opacity 0
      stagger: 0.2, // Delay between each image's animation
      ease: "back.out(1.7)", // Ease effect
    });
    gsap.to('.skill-title-4',{
      scrollTrigger:{
        trigger:'.skill-container4',
        start:'bottom 80%',
        scrub:1,
        end:'bottom 60%'
      },
      x:-300,
      opacity:0
    })

  },
};
</script>
