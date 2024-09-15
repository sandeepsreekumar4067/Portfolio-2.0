<template>
  <div class="second-page-container" >
    <div class="about-me-container">
      <span>A</span>
      <span>b</span>
      <span>o</span>
      <span>u</span>
      <span>t</span>
      <span>M</span>
      <span>e</span>
    </div>
    <div class="about-me-description">
      I'm a Full Stack Developer with a focus on web and mobile applications. I
      specialize in Frontend Development using HTML, CSS, JavaScript, React, and
      Vue.js, and also work on the backend with Python , Node , express.
      Currently, I'm pursuing a B.Tech in Computer Science and Engineering at
      VJCET.I'm also Proficient in creating Mobile Applications using Flutter
      I'm passionate about building intuitive and impactful digital solutions
    </div>
    <div class="about-me-areas">
      <span id="explore"> My Specialities </span>
      <div class="speciality-description">
        <span>
          <img :src="fullStack" class="speciality-image" alt="" id="img1" />
          <div class="title">Full Stack Development</div>
          <div class="description">
            I build comprehensive web and mobile applications by combining
            frontend and backend technologies. I create interactive and
            responsive UIs with React , Vue.js and Angluar while ensuring smooth
            backend operations using Python , FastAPI , Node.js , Express.js .
            My goal is to deliver end-to-end solutions that work seamlessly
            across devices.
          </div>
        </span>
        <span>
          <img :src="frontEnd" class="speciality-image" alt="" id="img2"/>
          <div class="title">Frontend Development</div>
          <div class="description">
            I craft dynamic and user-friendly interfaces with HTML, CSS,
            JavaScript, and frameworks like Vue.js , React and Angular. My
            expertise in responsive design and GSAP animations ensures that each
            website not only functions flawlessly but also delivers an engaging
            visual experience across different platforms.
          </div>
        </span>
        <span>
          <img :src="mobileDev" class="speciality-image" alt="" id="img2"/>
          <div class="title">Mobile Application Development</div>
          <div class="description">
            Using Flutter, I develop cross-platform mobile apps with a focus on
            performance, user experience, and consistency. Whether it's for
            iOS or Android, I ensure that my apps deliver a smooth,
            intuitive experience, tailored to user needs and modern design
            principles
          </div>
        </span>
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/secondpage.css";
import frontEnd from "../assets/frontend(3).png";
import fullStack from "../assets/fullstack.png";
import mobileDev from "../assets/mobileDev.png";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      frontEnd: frontEnd,
      fullStack: fullStack,
      mobileDev: mobileDev,
    };
  },
  mounted(){
    gsap.registerPlugin(ScrollTrigger)
    gsap.from('.about-me-container',{
        scrollTrigger:{
        trigger:'.about-me-container',
        start:'top 60%',
        toggleActions:'play none none none'
      },
      duration:0.8,
      border:'solid 0px black',
      ease:'power2.inOut'
    })
    gsap.from('.about-me-container span',{
      scrollTrigger:{
        trigger:'.about-me-container span',
        start:'top 50%',
        toggleActions:'play none none none'
      },
      x:-100,
      opacity:0,
      delay:0.8,
      duration:0.5,
      stagger:0.2,
      ease:'power3.inOut'
    })
    gsap.from('.about-me-description',{
        scrollTrigger:{
        trigger:'.about-me-description',
        start:'top 60%',
        toggleActions:'play none none none'
      },
      x:'-10%',
      opacity:0,
      duration:1,
    })
    gsap.from('#explore',{
        scrollTrigger:{
            trigger:'#explore',
            start:'top 70%',
            toggleActions:'play none none none'
        },
        y:-100,
        duration:1,
        opacity:0,
        ease:'bounce.out'
    })
    gsap.from('.title',{
        scrollTrigger:{
            trigger:'.speciality-description',
            start:'top 70%',
            toggleActions:'play none none none'
        },
        x:-100,
        duration:1,
        ease:'power3.inOut',
        opacity:0,
        stagger:0.2
    })
    gsap.from('.description',{
        scrollTrigger:{
            trigger:'.speciality-description',
            start:'top 70%',
            toggleActions:'play none none none'
        },
        delay:0.3,
        x:-100,
        duration:1,
        ease:'power3.inOut',
        opacity:0,
        stagger:0.2
    })
    gsap.from('.speciality-image',{
        scrollTrigger:{
            trigger:'.speciality-description',
            start:'top 70%',
            toggleActions:'play none none none'
        },
        delay:1,
        x:-155,
        duration:1,
        ease:'power3.inOut',
        opacity:1,
        stagger:0.2
    })
  }
};
</script>

<style>
</style>