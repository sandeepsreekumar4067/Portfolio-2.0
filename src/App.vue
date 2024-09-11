<template>
  <HomePage/>
</template>

<script>
import HomePage from './components/HomePage.vue';
import './Style/app.css'
import 'bootstrap-icons/font/bootstrap-icons.css';  // Import Bootstrap CSS


export default {
  name: 'App',
  components: {
    HomePage,
    // SecondPage,
    // // ThirdPage
  }
}
</script>