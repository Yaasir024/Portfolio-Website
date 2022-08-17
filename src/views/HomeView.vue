<script setup>
import Hero from "../components/Hero.vue";
import Projects from "../components/Projects.vue";
import Articles from "../components/Articles.vue";
import Cta from "../components/Cta.vue";
</script>

<template>
  <div class="main">
    <div class="hero-section">
      <Hero />
    </div>
    <main class="main-content">
      <Projects />
      <Articles />
      <Cta />
      <footer>Built with 💻 and ☕ by Yaasir Falana</footer>
    </main>
  </div>
</template>
<style scoped>
.main {
  /* display: flex; */
}
.hero-section {
  position: sticky;
  top: 0;
  width: 100%;
  height: 100%;
  transition: width 1s cubic-bezier(0.23, 1, 0.32, 1);
}
.main-content {
  background: var(--color-background);
  min-height: 100vh;
  padding: 0 12px;
}
footer {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  flex-direction: column;
  height: auto;
  min-height: 70px;
  padding: 40px 15px;
  text-align: center;
}
@media only screen and (min-width: 1150px) {
  .hero-section {
    width: 40%;
    position: fixed;
    left: 0;
    transition: width 1s cubic-bezier(0.23, 1, 0.32, 1) 0.5s;
    z-index: 3;
  }
  .main-content {
    width: 60%;
    margin-left: 40%;
  }
  .main-content {
    background: var(--color-background);
    min-height: 100vh;
    padding: 15px 12px;
  }
}
</style>
