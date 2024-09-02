<template>
  <div class="home-container">
    <div class="home-title">
        Hello
    </div>
    <div class="home-name">
        I'm <span>Sandeep Sreekumar</span>
    </div>
    <div class="home-about">
        I'm a <span id="typewriter-about"></span>
    </div>
  </div>
</template>

<script>
import '../Style/homepage.css'
import Typewriter from 'typewriter-effect/dist/core';
import { gsap } from 'gsap';
export default {
    name:'HomePage',
    data(){
        return{

        }
    },
    mounted(){
       const typeWiterAbout = new Typewriter ('#typewriter-about',{
        strings:['Front-End Developer ','Back-End Developer '],
        autoStart:true,
        loop:true,
        delay:75
       })
       typeWiterAbout.start()
       gsap.from('.home-title',{
        opacity:0,
        duration:1,
        y:100
       })
       gsap.from('.home-name',{
        y:100,
        duration:1,
        delay:0.2,
        opacity:0,
       })
       gsap.from('.home-about',{
        opacity:0,
        y:100,
        duration:1,
        delay:0.4
       })
    }
}
</script>

<style>

</style>