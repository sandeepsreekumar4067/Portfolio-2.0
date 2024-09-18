<template>
  <div class="fourth-page-container">
    <span></span><span></span><span></span><span></span>
  </div>
</template>

<script>
import '../Style/fourthpage.css'
import {gsap} from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger';
export default {
    mounted(){
        gsap.registerPlugin(ScrollTrigger)
        gsap.utils.toArray('.fourth-page-container span').forEach((span)=>{
            gsap.from(span,{
                scrollTrigger:{
                    trigger:span,
                    start:'top 90%',
                    scrub:1,
                    end:'center center'
                },
                scale:0
            },)
        })
   
    }
}
</script>

