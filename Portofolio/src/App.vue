<script setup lang="ts">
import TheWelcome from './components/TheWelcome.vue'
import NavBar from './components/NavBar.vue'
import HeroSection from './components/HeroSection.vue';
import AboutSection from './components/AboutSection.vue';
</script>

<template>
  <header>
    <NavBar />  
  </header>

  <main>
    <HeroSection />
    <AboutSection />
  </main>
</template>

<style scoped>


/* @media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    flex-direction: column;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
} */
</style>
