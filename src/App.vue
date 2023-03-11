<template>
<NavigationBar/>
<HeroSection/>
<DescriptionSection/>
<DoctorSection/>
</template>

<script>
import NavigationBar from './components/NavigationBar.vue'
import HeroSection from './components/HeroSection.vue'
import DescriptionSection from './components/DescriptionSection.vue'
import DoctorSection from './components/DoctorSection.vue'


export default {
  name: 'App',
  components: {NavigationBar, HeroSection, DescriptionSection, DoctorSection},
}
</script>

<style>
@import './assets/variables.css';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
