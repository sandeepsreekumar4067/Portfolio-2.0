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
              <div class="proj-link">View</div>
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
          githubLink: "",
        },
        {
          title: "Tourism Promotion Website (MERN Stack)",
          description:
            "Designed and deployed a dynamic tourism website using the MERN stack, featuring visuals, interactive maps, and comprehensive travel guides for showcasing destinations.",
          projimage: projimg4,
          githubLink: "",
        },
        {
          title: "Vivavoce (Website)",
          description:
            "Developed Vivavoce, a website for blind students using Gemini technology, enabling tests through audio interfaces with personalized feedback and assessment.",
          projimage: projimg5,
          githubLink: "",
        },
        {
          title: "AI Legal Consultant Website",
          description:
            "Built an AI-powered legal platform using LangChain and RAG for backend and React for frontend, featuring text extraction, conversational AI, and a responsive chat interface.",
          projimage: projimg6,
          githubLink: "",
        },
        {
          title: "Space Exploration App (Flutter)",
          description:
            "Created a Flutter app providing space exploration information, with captivating visuals and real-time data on missions, celestial bodies, and astronomical events.",
          projimage: projimg7,
          githubLink: "",
        },
        {
          title: "Review O (Intern at FSH Design)",
          description:
            "Developed frontend interfaces with Vue.js and backend functionalities using Python and MySQL for a professional review system helping MNCs analyze customer satisfaction.",
          projimage: projimg8,
          githubLink: "",
        },
        {
          title: "Mint Investing (Intern at FSH Design)",
          description:
            "Developed the backend using Python FastAPI and integrated MySQL for an investment platform, creating efficient API endpoints for mobile app data management.",
          projimage: projimg9,
          githubLink: "",
        },
        {
          title: "Library Management System (Web)",
          description:
            "Developed a web-based library management system for cataloging, circulation, and administration, featuring book search, borrower management, and transaction tracking.",
          projimage: projimg10,
          githubLink: "",
        },
        {
          title: "ByTheFans (Intern at FSH Design)",
          description:
            "Enhanced frontend development for a community platform for sports enthusiasts, allowing fans to share updates and engage with like-minded individuals.",
          projimage: projimg11,
          githubLink: "",
        },
        {
          title: "Book Reselling Website (Web)",
          description:
            "Created a scalable platform for buying and selling second-hand books with features such as user profiles, listings, and secure payment gateways.",
          projimage: projimg12,
          githubLink: "",
        },
        {
          title: "Supermarket Prediction Model (Python Data Science)",
          description:
            "Implemented a predictive model for supermarket inventory management using Python, optimizing stock levels and reducing waste with machine learning algorithms.",
          projimage: projimg13,
          githubLink: "",
        },
        {
          title: "Dictionary App (Flutter)",
          description:
            "Developed a user-friendly dictionary app with features like search functionality and word suggestions for quick and efficient word lookup.",
          projimage: projimg14,
          githubLink: "",
        },
      ],
    };
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