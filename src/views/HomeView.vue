<template>
  <div class="hellmanns-app">
    <Header />
    <HeroSection />
    <ParticipateChallengeSection />
    <RankingSection />
    <PlayGuideSection />
    <Footer />
  </div>
</template>

<script>
import Header from '../components/Header.vue'
import HeroSection from '../components/HeroSection.vue'
import ParticipateChallengeSection from '../components/ParticipateChallengeSection.vue'
import RankingSection from '../components/RankingSection.vue'
import PlayGuideSection from '../components/PlayGuideSection.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'HomeView',
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

<style scoped>
.hellmanns-app {
  min-height: 100vh;
  width: 100%;
  background-color: #fff;
  margin: 0;
  padding: 0;
}
</style>
