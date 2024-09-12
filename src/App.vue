<template>
 <div class="panel">
  <HomePage />
 </div>
 <div class="panel">
   <SecondPage/>
 </div>
</template>

<script>
import HomePage from './components/HomePage.vue';
import SecondPage from './components/SecondPage.vue';
import './Style/app.css'
import 'bootstrap-icons/font/bootstrap-icons.css';  // Import Bootstrap CSS
export default {
  name: 'App',
  components: {
    HomePage,
    SecondPage,
    // // ThirdPage
  },
  mounted(){
   
  }
}
</script>