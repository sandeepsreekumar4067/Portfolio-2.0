<template>
  <HomePage id="panel1" />
  <SecondPage id="panel2" />
  <ThirdPage />
</template>

<script>
import HomePage from "./components/HomePage.vue";
import SecondPage from "./components/SecondPage.vue";
import ThirdPage from "./components/ThirdPage.vue";
import "./Style/app.css";
import "bootstrap-icons/font/bootstrap-icons.css"; // Import Bootstrap CSS
export default {
  name: "App",
  components: {
    HomePage,
    SecondPage,
    ThirdPage,
  },
};
</script>
<style>
</style>