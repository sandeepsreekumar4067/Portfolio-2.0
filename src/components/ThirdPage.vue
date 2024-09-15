<template>
  <div class="third-page-container" id="tmain">
    <div class="third-page-components" id="components">
      <div class="circle">My Skills</div>
      <div class="skill-container">
        <div class="rows">
          <span>

          </span>
        </div>
        <div class="rows"></div>
        <div class="rows"></div>
        <div class="rows"></div>
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
import python from "../assets/languageIcons/python.png"
import java from "../assets/languageIcons/java.png"
import js from "../assets/languageIcons/js.png"
import dart from "../assets/languageIcons/dart.png"
import experss from "../assets/languageIcons/expressjs.png"
import vue from "../assets/languageIcons/vueJs.png"
import firebase from "../assets/languageIcons/fireabase.png"
import flutter from "../assets/languageIcons/flutter.png"
import react from "../assets/languageIcons/react.png"
import node from "../assets/languageIcons/nodejs.png"
import mongo from "../assets/languageIcons/mongoDb.png"
import spline from "../assets/languageIcons/spline.png"
import ts from "../assets/languageIcons/typescript.png"
import mySql from "../assets/languageIcons/mySql.png"
import html from "../assets/languageIcons/html.png"
import css from "../assets/languageIcons/css.png"
import github from "../assets/languageIcons/github.png"

export default {
  data(){
    return{
      c:c,
      cpp:cpp,
      python:python,
      java:java,
      js:js,
      dart:dart,
      experss:experss,
      vue:vue,
      firebase:firebase,
      flutter:flutter,
      react:react,
      node:node,
      mongo:mongo,
      spline:spline,
      ts:ts,
      mySql:mySql,
      html:html,
      css:css,
      github:github,
      pl:[c,cpp,python,java,js],
      wd:[html,css,react,vue,node,experss],
      md:[flutter],
      db:[firebase,mySql,mongo],
      tools:[github]
    }
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    // const timeline = gsap.timeline({
    //   scrollTrigger: {
    //     trigger: "#components",
    //     markers: true,
    //     start: "top 10%",
    //     pin: true,
    //     scrub: 1,
    //     endTrigger: "#tmain",
    //     end: "bottom bottom",
    //     toggleActions: 'play reverse play reverse', // Ensures the animation reverses when scrolling back up
    //   },
    // });
    // timeline.from(".circle", {
    //   opacity: 0,
    //   x:-300
    // });
    // timeline.from('.skill-container',{
    //   width:'2rem',
    //   height:'2rem',
    //   opacity:0,    
    //   snap:1
    // })
  },
};
</script>

