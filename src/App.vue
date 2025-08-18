<template>
  <div id="app">
    <AppHeader />
    <HeroSection />
    <DescriptionSection />
    <PremiosSection />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import DescriptionSection from './components/DescriptionSection.vue'
import PremiosSection from './components/PremiosSection.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    HeroSection,
    DescriptionSection,
    PremiosSection
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

html, body {
  overflow-x: hidden;
}
</style>
