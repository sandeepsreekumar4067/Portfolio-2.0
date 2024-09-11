<template>
  <div class="homepage-container">
    <div class="wrapper">
      <div class="left-container">
        <div class="left-about-container">
          <div class="left-title">Hi I'm</div>
          <div>
            <div class="left-name">Sandeep Sreekumar</div>
            <div class="left-desc">Frontend Developer / Full Stack</div>
          </div>
        </div>
        <div class="left-button-container">
          <span>
            <i class="bi bi-github"></i>
          </span>
          <span>
            <i class="bi bi-linkedin"></i>
          </span>
          <span>
            <i class="bi bi-instagram"></i>
          </span>
          <span>
            <i class="bi bi-twitter-x"></i>
          </span>
        </div>
      </div>
      <div class="right-container">
        <img :src="homeImage" alt="" />
      </div>
    </div>
    <div class="bottom-container">
      <span>Hey Guys</span>
      I'm a Full Stack Developer with a focus on web and mobile applications. I
      specialize in Frontend Development using HTML, CSS, JavaScript, React, and
      Vue.js, and also work on the backend with Python and FastAPI. Currently,
      I'm pursuing a B.Tech in Computer Science and Engineering at VJCET. I'm
      passionate about building intuitive and impactful digital solutions
    </div>
  </div>
</template>

<script>
import "../Style/homepage.css";
import homeImage from "../assets/homeImage2.png";
export default {
  data() {
    return {
      homeImage: homeImage,
    };
  },
};
</script>
