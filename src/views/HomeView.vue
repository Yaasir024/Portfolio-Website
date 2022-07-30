<script setup>
import Hero from "../components/Hero.vue";
import Projects from "../components/Projects.vue";
</script>

<template>
  <div class="main">
    <div class="hero-section">
      <Hero />
    </div>
    <main class="main-content">
      <Projects />
    </main>
  </div>
</template>
<style scoped>
.main {
  display: flex;
}
.hero-section {
  max-width: 496px;
  position: fixed;
}
.main-content {
  position: absolute;
  right: 0;
  max-width: 535px;
}
</style>
