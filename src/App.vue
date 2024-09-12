<template>
 <div class="panel">
  <HomePage />
 </div>
 <div class="panel">
  <SecondPage/>
 </div>
</template>

<script>
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';
import './Style/app.css'
import 'bootstrap-icons/font/bootstrap-icons.css';  // Import Bootstrap CSS
import { gsap } from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
export default {
  name: 'App',
  components: {
    HomePage,
    SecondPage,
    // // ThirdPage
  },
  mounted(){
    gsap.registerPlugin(ScrollTrigger)
    gsap.utils.toArray('.panel').forEach((panel)=>{
      ScrollTrigger.create({
        trigger:panel,
        start:'top top',
        pin:true,
        pinSpacing:false
      })
    })
  }
}
</script>