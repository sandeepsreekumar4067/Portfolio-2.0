<template>
  <HomePage/>
  <SecondPage/>
</template>

<script>
import './Style/app.css'
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';


export default {
  name: 'App',
  components: {
    HomePage,
    SecondPage
  }
}
</script>