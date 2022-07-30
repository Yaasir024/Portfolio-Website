<template>
  <div class="hero">
    <div class="top">
      <div class="details">
        <h2>Oi, I'm</h2>
        <h1 class="name">Yaasir Falana</h1>
        <h2 class="profession">Frontend Web Developer</h2>
        <p class="about">
          Goal-oriented Frontend Developer with experience in web design and
          development.
        </p>
        <p class="about">
            Proficient in HTML, CSS, JavaScript with modern
          frameworks and libraries. Innovative, creative and a great team
          player.
        </p>
      </div>
      <nav>
        <ul>
          <li>Works</li>
          <li>Projects</li>
        </ul>
      </nav>
    </div>
    <div class="bottom">
      <p>Twitter</p>
    </div>
  </div>
</template>

<style scoped>
.hero {
  padding: 55px 45px;
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.hero .top .details {
  padding-top: 20px;
}
.name {
  font-size: 46px;
  font-weight: 700;
  line-height: 1.5;
}
.profession {
  font-size: 26px;
  font-weight: 600;
  margin-top: 10px;
}
.about {
    font-size: 14px;
    color: var(--color-text-secondary);
}
.hero .top nav {
  margin-top: 72px;
}
</style>
