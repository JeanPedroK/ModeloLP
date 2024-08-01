<script setup>
import MainTitle from './components/MainTitle.vue'
import MainSection from './components/MainSection.vue'
import NavBar from './components/NavBar.vue'
</script>

<template>
  <NavBar />
  <MainTitle msg="Modelo Landing Page" />
  <MainSection />
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
