<template>
  <div class="fourth-wrapper" id="fmain">
    <div class="fourth-page-container" id="fcomp">
      <div class="background-image">
        <img :src="mountainImage" alt="" />
      </div>
      <div class="fourth-page-components">
        <div class="fourth-page-title">
          <span>Projects</span>
        </div>
        <div class="project-components">
          <span v-for="(project, key) in projects" :key="key">
            <img :src="project.projimage" alt="" />
            <div class="proj-span">
              <div class="proj-title">{{ project.title }}</div>
              <div class="proj-desc">{{ project.description }}</div>
              <div class="proj-link" @click="openProject(project.githubLink)">View</div>
            </div>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import "../Style/fourthpage.css";
import mountainImage from "../assets/background/mountainImage.jpg";
import projimg3 from "../assets/project images/img3.png";
import projimg4 from "../assets/project images/img1 (2).jpg";
import projimg5 from "../assets/project images/img5.jpg";
import projimg6 from "../assets/project images/img6.png";
import projimg7 from "../assets/project images/img7.jpg";
import projimg8 from "../assets/project images/img8.jpg";
import projimg9 from "../assets/project images/img9.png";
import projimg10 from "../assets/project images/img10.jpg";
import projimg11 from "../assets/project images/img11.jpg";
import projimg12 from "../assets/project images/img12.jpg";
import projimg13 from "../assets/project images/img13.jpg";
import projimg14 from "../assets/project images/img14.jpg";

import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";
export default {
  data() {
    return {
      mountainImage: mountainImage,
      projimg3: projimg3,
      projimg4: projimg4,
      projimg5: projimg5,
      projimg6: projimg6,
      projimg7: projimg7,
      projimg8: projimg8,
      projimg9: projimg9,
      projimg10: projimg10,
      projimg11: projimg11,
      projimg12: projimg12,
      projimg13: projimg13,
      projimg14: projimg14,
      projects: [
        {
          title: "Lex Ai",
          description:
            "This project is a backend for an AI legal consultant utilizing LangChain to manage a Large Language Model (LLM). It includes Python scripts like `casualBot.py` and `lawyerBot.py` to handle various user interactions and provide legal advice. LangChain enhances the AI's ability to process and interpret complex legal queries.",
          projimage: projimg3,
          githubLink: "https://github.com/sandeepsreekumar4067/LexAi-backend",
        },
        {
          title: "Tourism Promotion Website (MERN Stack)",
          description:
            "Designed and deployed a dynamic tourism website using the MERN stack, featuring visuals, interactive maps, and comprehensive travel guides for showcasing destinations.",
          projimage: projimg4,
          githubLink: "https://github.com/sandeepsreekumar4067/ww",
        },
        {
          title: "MyAnswer (Website)",
          description:
            "Developed MyAnswer, a website for blind students using Gemini technology, enabling tests through audio interfaces with personalized feedback and assessment.",
          projimage: projimg5,
          githubLink: "https://github.com/sandeepsreekumar4067/My-Answer",
        },
        {
          title: "AI Legal Consultant Website",
          description:
            "Built an AI-powered legal platform using LangChain and RAG for backend and React for frontend, featuring text extraction, conversational AI, and a responsive chat interface.",
          projimage: projimg6,
          githubLink: "https://github.com/sandeepsreekumar4067/main-project",
        },
        {
          title: "Space Elevator (Flutter)",
          description:
            "Created a Flutter app providing space exploration information, with captivating visuals and real-time data on missions, celestial bodies, and astronomical events.",
          projimage: projimg7,
          githubLink: "https://github.com/sandeepsreekumar4067/SpaceElevator",
        },
        {
          title: "Review O (Intern at FSH Design)",
          description:
            "(Due to confidential nature i cannot share the code )Developed frontend interfaces with Vue.js and backend functionalities using Python and MySQL for a professional review system helping MNCs analyze customer satisfaction.",
          projimage: projimg8,
          githubLink: "",
        },
        {
          title: "Mint Investing (Intern at FSH Design)",
          description:
            "(Due to confidential nature i cannot share the code )Developed the backend using Python FastAPI and integrated MySQL for an investment platform, creating efficient API endpoints for mobile app data management.",
          projimage: projimg9,
          githubLink: "",
        },
        {
          title: "ByTheFans (Intern at FSH Design)",
          description:
            "(Due to confidential nature i cannot share the code )Enhanced frontend development for a community platform for sports enthusiasts, allowing fans to share updates and engage with like-minded individuals.",
          projimage: projimg11,
          githubLink: "",
        },
        {
          title: "Ktu QP Scrapper",
          description:
            "The KTU Question Paper Scraper API allows students to quickly and easily retrieve past exam papers from Kerala Technological University (KTU) for study purposes, automating the process of searching and downloading.",
          projimage: projimg10,
          githubLink: "https://github.com/sandeepsreekumar4067/KTU-qp-scapper",
        },
        {
          title: "Book Reselling Website (Web)",
          description:
            "Created a scalable platform for buying and selling second-hand books with features such as user profiles, listings, and secure payment gateways.",
          projimage: projimg12,
          githubLink: "https://github.com/sandeepsreekumar4067/bookbuddies",
        },
        {
          title: "Pawssible",
          description:
            "created a website that connects breeders, enabling them to buy and sell pets easily. The platform offers listings for various types of pets, providing a user-friendly interface for breeders to post ads, browse available pets, and make transactions seamlessly.",
          projimage: projimg13,
          githubLink: "https://github.com/sandeepsreekumar4067/pawssible",
        },
        {
          title: "Wallet App (Flutter)",
          description:
            "created a Flutter-based wallet app that allows users to manage their finances, track transactions, and store digital currencies. The app features a clean, intuitive interface, ensuring secure and seamless financial management on mobile devices.",
          projimage: projimg14,
          githubLink: "https://github.com/sandeepsreekumar4067/Flutter-Wallet-App",
        },
      ],
    };
  },
  methods:{
    openProject(link){
      window.open(link,'_blank')
    }
  },
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    const tl = gsap.timeline({
      scrollTrigger: {
        trigger: "#fcomp",
        start: "top top",
        pin: true,
        endTrigger: "#fmain",
        end: "bottom bottom",
        toggleActions: "play none replay reverse"
      },
    });
    tl.from(".fourth-page-title", {
      x: -100,
      opacity: 0,
    });
    tl.from(".project-components", {
      yPercent: 100,
      duration: 1.5,
    });
    tl.from(".project-components span", {
      scale: 0,
      ease: "circ.inOut",
      stagger: 0.2,
    });
  },
};
</script>

<style>
</style>