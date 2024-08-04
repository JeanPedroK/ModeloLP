<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue';
import MainTitle from './components/MainTitle.vue'
import NavBar from './components/NavBar.vue'
import Servicos from '../src/components/Sections/Servicos.vue'
import Features from '../src/components/Sections/Features.vue'
import Pacotes from '../src/components/Sections/Pacotes.vue'
import Testimonials from '../src/components/Sections/Testimonial.vue'
import Slider from '../src/components/Sections/Slider.vue'
import MediaSocial from './components/Sections/MediaSocial.vue';

var menusNav = [{ name: '#homePage', title:"Home", status:'ativo', submenu: false },
{ name: '#services', title:"Serviços", status:'ativo', submenu: false },
{ name: '#features', title:"Features", status:'ativo', submenu: false },
{ name: '#prices', title:"Pacotes", status:'ativo', submenu: false },
]

var activeSection = ref('homePage');

const onScroll = () => {
  const sections = ['homePage', 'services', 'features', 'prices'];

  for (const section of sections) {
    const element = document.getElementById(section);
    const rect = element.getBoundingClientRect();
    if (rect.top >= 0 && rect.top <= window.innerHeight / 2) {

      activeSection.value = section;

      break;
    }
  }
};

onMounted(() => {
  window.addEventListener('scroll', onScroll);


});

onBeforeUnmount(() => {
  window.removeEventListener('scroll', onScroll);
});


</script>

<template>
  <NavBar :menuOptions= "menusNav" :ativa="activeSection"  />
  <MainTitle msg="Modelo Landing Page" id="homePage" />
  <Servicos id="services" />
  <Features id="features" />
  <Pacotes id="prices" />
  <Testimonials />
  <Slider />
  <MediaSocial />
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
