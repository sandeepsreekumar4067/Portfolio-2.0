<template>
  <div class="last-page-container">
    <div class="contact-title">
        Contact
    </div>
    <div class="resume">
        Download my resume <span>Here</span>
    </div>
    <div class="social-media">
        <div class="social-title">
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
export default {
    data(){
        return{
            instagram:instagram,
            twitterX:twitterX,
            linkedin:linkedin,
            github:github
        }
    }
}
</script>

<style>

</style>