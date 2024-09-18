<template>
  <div class="fourth-page-container">
    <div class="project-container">
      <img :src="neonImg" alt="" />
      <div class="cover-container">
        <div class="project-title">Lex Ai (backend)</div>
        <div class="project-content">
          <div class="project-left">project Link</div>
          <div class="project-right">
            This project is the backend for an AI legal consultant using
            LangChain technology to control a Large Language Model (LLM). It
            includes various components like `casualBot.py` and `lawyerBot.py`
            to handle different types of user interactions, potentially offering
            legal advice or information. The use of LangChain suggests advanced
            AI capabilities for managing and interpreting complex legal queries,
            while Python scripts manage tasks like data processing, training,
            and interactions with the LLM.
          </div>
        </div>
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
    gsap.utils.toArray(".project-container").forEach((span) => {
      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: span,
          start: "top 90%",
          end: "top 5%",
          scrub: 1,
        },
      });
      tl.from(span, {
        scale: 0,
      });
      tl.to(span, {
        scale: 0,
      });
    });
  },
};
</script>

