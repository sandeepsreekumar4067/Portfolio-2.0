<template>
  <HomePage/>
  <SecondPage/>
  <!-- <ThirdPage/> -->
</template>

<script>
import './Style/app.css'
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';
// import ThirdPage from './components/ThirdPage.vue';


export default {
  name: 'App',
  components: {
    HomePage,
    SecondPage,
    // ThirdPage
  }
}
</script>