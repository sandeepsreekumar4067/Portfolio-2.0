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
        const spans = document.querySelectorAll('.secondPage-container span')
        spans.forEach((span)=>{
            gsap.fromTo(span,{
                opacity:0,
                y:100
            },{
                opacity:1,
                y:0,
                scrollTrigger:{
                    trigger:span,
                    start:'top 90%',
                    end:'top 20%',
                    scrub:true,

                    toggleActions: 'play reverse play reverse',
                    onEnter:()=>{
                        gsap.to(span,{opacity:1,y:0,})
                    },
                    onLeave:()=>{
                        gsap.to(span,{opacity:0,y:-100,})
                    },
                    
                }
            })
        })
    }
};
</script>

<style>
</style>