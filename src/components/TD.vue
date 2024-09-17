<template>
  <div class="third-page-container">
    <div class="skill-title">My Skills</div>
    
  </div>
</template>
  

  <script>
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import "../Style/td.css";
// Importing icons
import c from "../assets/languageIcons/c.png";
import cpp from "../assets/languageIcons/c++.png";
import python from "../assets/languageIcons/python.png";
import java from "../assets/languageIcons/java.png";
import js from "../assets/languageIcons/js.png";
import dart from "../assets/languageIcons/dart.png";
import express from "../assets/languageIcons/expressjs.png";
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
import github from '../assets/languageIcons/github.png'
export default {
  data() {
    return {
      // Skills array with names and icons
      c: c,
      cpp: cpp,
      python: python,
      java: java,
      js: js,
      dart: dart,
      experss: express,
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
      github:github,
      skills: [
        { icon: c, name: "C" },
        { icon: cpp, name: "C++" },
        { icon: python, name: "Python" },
        { icon: java, name: "Java" },
        { icon: js, name: "JavaScript" },
        { icon: dart, name: "Dart" },
        { icon: express, name: "Express.js" },
        { icon: vue, name: "Vue.js" },
        { icon: firebase, name: "Firebase" },
        { icon: flutter, name: "Flutter" },
        { icon: react, name: "React" },
        { icon: node, name: "Node.js" },
        { icon: mongo, name: "MongoDB" },
        { icon: spline, name: "Spline" },
        { icon: ts, name: "TypeScript" },
        { icon: mySql, name: "MySQL" },
        { icon: html, name: "HTML" },
        { icon: css, name: "CSS" },
      ],
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    // Animate each skill box to pop in
    // gsap.utils.toArray(".skill-box").forEach((box, index) => {
    //   gsap.from(box, {
    //     scrollTrigger: {
    //       trigger: box,
    //       start: "top 80%",
    //       end: "top 60%",
    //       scrub: 1,
    //     },
    //     x: index % 2 === 0 ? -200 : 200, // Slide from left or right
    //     opacity: 0,
    //     duration: 1,
    //   });
    // });

    // // Animate the vertical line
    // gsap.from(".line", {
    //   scrollTrigger: {
    //     trigger: ".skills-timeline",
    //     start: "top 30%",
    //     end: "bottom 60%",
    //     scrub: 1,
    //   },
    //   height: 0,
    //   duration: 1,
    // });
  },
};
</script>
  