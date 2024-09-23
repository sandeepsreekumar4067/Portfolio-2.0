<template>
  <div class="last-page-container">
    <div class="contact-title">
        Contact
    </div>
    <div class="resume" id="common">
        Download my resume <span>Here</span>
    </div>
    <div class="social-media">
        <div class="social-title" id="common">
            You can also find me On
        </div>
        <div class="social-media-components">
            <span>
                <img :src="instagram" alt="">
                <p>Instagram</p>
            </span>
            <span>
                <img :src="linkedin" alt="">
                <p>Linkedin</p>
            </span>
            <span>
                <img :src="github" alt="">
                <p>Github</p>
            </span>
            <span>
                <img :src="twitterX" alt="">
                <p>X</p>
            </span>
        </div>
            <div class="end-text">
                Hit me up on my Social Media <br>
                Lets create innovative Projects
            </div>
    </div>
  </div>
</template>

<script>
import instagram from '../assets/socialmeda/instagram.svg'
import twitterX from '../assets/socialmeda/twitter-x.svg'
import linkedin from '../assets/socialmeda/linkedin-icon-2.svg'
import github from '../assets/socialmeda/github.svg'
import '../Style/lastpage.css'
import {gsap} from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'
export default {
    data(){
        return{
            instagram:instagram,
            twitterX:twitterX,
            linkedin:linkedin,
            github:github
        }
    },
    mounted(){
        gsap.registerPlugin(ScrollTrigger)
        gsap.from('.contact-title',{
            scrollTrigger:{
                trigger:'.contact-title',
                start:'top 50%',
            },
            y:-100,
            opacity:0,
            ease:'bounce.out',
            duration:1.2
        })
        gsap.from('#common',{
            scrollTrigger:{
                trigger:'#common',
                start:'top 50%',
            },
            y:100,
            opacity:0,
            stagger:0.3,
            duration:1.2
        })
        gsap.from('.social-media-components span',{
            scrollTrigger:{
                trigger:'.social-media-components',
                start:'top 50%',
            },
            delay:1,
            scale:0,
            stagger:0.4,
            ease:'bounce.out',
            duration:1
        })
        gsap.from('.end-text',{
            scrollTrigger:{
                trigger:'.end-text',
                start:'top 90%',
            },
            x:100,
            opacity:0,
            duration:0.9
        })
    }
}
</script>

<style>

</style>