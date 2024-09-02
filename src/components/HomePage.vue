<template>
  <div class="home-container">
    <div class="home-title">
        Hello
    </div>
    <div class="home-name">
        Im <span>Sandeep Sreekumar</span>
    </div>
    <div class="home-about">
        Im a <span id="typewriter-about"></span>
    </div>
  </div>
</template>

<script>
import '../Style/homepage.css'
import Typewriter from 'typewriter-effect/dist/core';
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
    }
}
</script>

<style>

</style>