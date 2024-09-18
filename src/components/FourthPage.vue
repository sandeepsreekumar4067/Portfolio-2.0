<template>
  <div class="fourth-page-container">
    <div class="project-container">
      <video autoplay muted loop>
        <source :src="neonVideo" type="video/mp4">
      </video>
    </div>
  </div>
</template>

<script>
import "../Style/fourthpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import neonVideo from '../assets/videos/neon abstract 1.mp4'
export default {

    data(){
        return{
            neonVideo:neonVideo
        }
    },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    // gsap.utils.toArray('.fourth-page-container span').forEach((span)=>{
    //     const tl = gsap.timeline({
    //         scrollTrigger:{
    //             trigger:span,
    //             start:'top 90%',
    //             end:'top 5%',
    //             scrub:1
    //         }
    //     })
    //     tl.from(span,{
    //         scale:0
    //     })
    //     tl.to(span,{
    //         scale:0
    //     })
    // })
  },
};
</script>

