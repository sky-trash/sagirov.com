<script>
import HeaderComponent from './components/HeaderComponent.vue'
import HeroSection from './components/HeroSection.vue'
import QuestionsSection from './components/QuestionsSection.vue'
import FooterComponent from './components/FooterComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    HeroSection,
    QuestionsSection,
    FooterComponent
  }
}
</script>
<template>
  <div class="app">
    <HeaderComponent />
    <HeroSection />
    <QuestionsSection />
    <FooterComponent />
  </div>
</template>

<style lang="scss">
@import './assets/main.scss';

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Inter', 'Arial', sans-serif;
  line-height: 1.6;
  color: #333;
  min-height: 100vh;
}

.app {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
}
</style>