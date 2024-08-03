<script setup>
// import { ref, onMounted, onBeforeUnmount } from 'vue';
import MainTitle from './components/MainTitle.vue'
import NavBar from './components/NavBar.vue'
import Servicos from '../src/components/Sections/Servicos.vue'
import Features from '../src/components/Sections/Features.vue'
import Pacotes from '../src/components/Sections/Pacotes.vue'


// const activeSection = ref('homePage');

// const onScroll = () => {
//   const sections = ['home', 'services', 'features', 'prices'];
//   for (const section of sections) {
//     const element = document.getElementById(section);
//     const rect = element.getBoundingClientRect();
//     if (rect.top >= 0 && rect.top <= window.innerHeight / 2) {
//       activeSection.value = section;
//       break;
//     }
//   }
// };

// onMounted(() => {
//   window.addEventListener('scroll', onScroll);
// });

// onBeforeUnmount(() => {
//   window.removeEventListener('scroll', onScroll);
// });
</script>

<template>
  <NavBar />
  <MainTitle msg="Modelo Landing Page" id="homePage"/>
  <Servicos id="services" />
  <Features id="features" />
  <Pacotes id="prices" />
</template>


<style scoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
