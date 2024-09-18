<template>
  <div class="fourth-page-container">
    <div class="project-container">
      <img :src="neonImg" alt="">
      <div class="cover-container">
        
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/fourthpage.css";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
import neonImg from "../assets/project images/img1 (1).jpg";
export default {
  data() {
    return {
      neonImg: neonImg,
    };
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    gsap.utils.toArray('.project-container').forEach((span)=>{
        const tl = gsap.timeline({
            scrollTrigger:{
                trigger:span,
                start:'top 90%',
                end:'top 5%',
                scrub:1
            }
        })
        tl.from(span,{
            scale:0
        })
        tl.to(span,{
            scale:0
        })
    })
  },
};
</script>

