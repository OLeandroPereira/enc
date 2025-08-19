<template>
  <div id="app">
    <Header />
    <HeroSection />
    <ParticipateChallengeSection />
    <RankingSection />
    <PlayGuideSection />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import ParticipateChallengeSection from './components/ParticipateChallengeSection.vue'
import RankingSection from './components/RankingSection.vue'
import PlayGuideSection from './components/PlayGuideSection.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    HeroSection,
    ParticipateChallengeSection,
    RankingSection,
    PlayGuideSection,
    Footer
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
