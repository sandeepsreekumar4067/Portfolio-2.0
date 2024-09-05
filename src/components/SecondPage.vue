<template>
  <div class="secondPage-container" id="sc-main">
    <div class="secondPage-display-container" id="sc-display">

    </div>
  </div>
</template>

<script>
import '../Style/secondpage.css'
import {gsap} from 'gsap'
export default {
    mounted(){
        gsap.from('#sc-display',{
            scrollTrigger:{
                trigger:'#sc-display',
                start:'top 0%',
                pin:true,
                toggleActions:'play pause reverse replay'
            },
            ease:'bounce.inOut',
            borderRadius:'50%',
            height:'10%',
            width:'10%'
        })
    }
}
</script>

<style>

</style>