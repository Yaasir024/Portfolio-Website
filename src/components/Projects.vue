<script setup>
import { ref, reactive } from "vue";
const projects = reactive([
  {
    title: "Rock Paper Scissors",
    img: "rps.PNG",
    about:
      "A minimal, dark blue theme for VS Code, Sublime Text, Atom, iTerm,and more. Available on Visual Studio Marketplace, Package Control,Atom Package Manager, and npm.",
    github: "https://github.com/Yaasir024/Rock-Paper-Scissors-Game",
    website: "https://rockpaperscissorsbyyaasir.netlify.app/",
  },
  {
    title: "Apple Website Clone",
    img: "appleclone.PNG",
    about: "A simple Clone of The front Page of Apple Website(UK).",
    github: "https://github.com/Yaasir024/Apple-clone",
    website: "https://appleclonebyyaasir.netlify.app/",
  },
  {
    title: "Hotel Landing Page",
    img: "konoha.PNG",
    about: "A simple game made with Vue 3 Composition Api.",
    github: "https://github.com/Yaasir024/konoha-hotel",
    website: "https://konohahotel.netlify.app/",
  },
  {
    title: "Movies Search App",
    img: "moviesapp.PNG",
    about: "A simple game made with Vue 3 Composition Api.",
    github: "https://github.com/Yaasir024/MoviesApp",
    website: "https://moviezapp.netlify.app/",
  },
  {
    title: "Baby Name Generator",
    img: "namegenerator.PNG",
    about: "A simple game made with Vue 3 Composition Api.",
    github: "https://github.com/Yaasir024/Baby-Name-Generator",
    website: "https://baby-namesgenerator.netlify.app/",
  },
]);
</script>

<template>
  <section class="projects-section">
    <div class="header">
      <span>Personal Projects</span>
    </div>
    <ul class="projects-container">
      <li
        class="project-card"
        v-for="(project, index) in projects"
        :key="index"
      >
        <div class="card-content">
          <h3 class="project-title">
            <a :href="`${project.website}`" target="_blank">{{ project.title }}</a>
          </h3>
          <div class="project-description">
            <p>
              {{ project.about }}
            </p>
          </div>
          <div class="project-links">
            <a
              :href="`${project.github}`"
              aria-label="GitHub Link"
              target="_blank"
              ><svg
                xmlns="http://www.w3.org/2000/svg"
                role="img"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="feather feather-github"
              >
                <title>GitHub</title>
                <path
                  d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"
                ></path>
              </svg>
            </a>
            <a
              :href="`${project.website}`"
              aria-label="External Link"
              class="external"
              rel="noopener noreferrer"
              target="_blank"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                role="img"
                viewBox="0 0 24 24"
                fill="none"
                stroke="currentColor"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                class="feather feather-external-link"
              >
                <title>External Link</title>
                <path
                  d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                ></path>
                <polyline points="15 3 21 3 21 9"></polyline>
                <line x1="10" y1="14" x2="21" y2="3"></line>
              </svg>
            </a>
          </div>
        </div>
        <div class="project-image">
          <a :href="`${project.website}`">
            <img :src="'/src/assets/projects/' + project.img" :alt="`${project.title}` + ' by Yaasir'" />
          </a>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.projects-section {
  padding: 55px 12px;
  width: 100%;
}
.header {
  margin-bottom: 20px;
}
.projects-container {
  list-style: none;
  padding: 0;
  margin-top: 20px;
}
.project-card {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  margin-bottom: 75px;
}
.project-card .card-content {
  position: relative;
  text-align: left;
}
.project-card:nth-of-type(2n + 1) .card-content {
  text-align: right;
}
.project-title {
  font-size: 22px;
  font-weight: 700;
  margin-bottom: 20px;
  z-index: 2;
}
.project-title a {
  font-weight: 700;
}
.project-description {
  position: relative;
  z-index: 2;
  padding: 25px;
  background: var(--color-background-soft);
  border-radius: 4px;
  font-size: 15px;
}

.project-links {
  display: flex;
  -webkit-box-align: center;
  align-items: center;
  position: relative;
  margin-top: 10px;
  margin-left: -10px;
  color: var(--color-text-secondary);
}
.project-card:nth-of-type(2n + 1) .project-links {
  -webkit-box-pack: end;
  justify-content: flex-end;
  margin-left: 0px;
  margin-right: -10px;
}

.project-links a {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  padding: 10px;
}
.project-links a svg {
  width: 20px;
  height: 20px;
}

.project-image {
  border-radius: 4px;
  overflow: hidden;
  box-shadow: 0 3px 10px rgb(0 0 0 / 0.2);
  transition: all 0.3s ease;
  background: beige;
  width: 100%;
}
.project-image:hover {
  transform: scale(1.02);
}
.project-image img {
  max-height: 280px;
  width: 100%;
  height: 100%;
  vertical-align: middle;
  /* mix-blend-mode: multiply;
    filter: grayscale(100%) contrast(1); */
}
@media only screen and (max-width: 1150px) {
  .projects-section {
    padding: 55px 0px;
    width: 100%;
  }
  .projects-container {
    max-width: 820px;
    margin: 0 auto;
    padding: 0 25px;
  }
}
@media only screen and (max-width: 750px) {
}

@media only screen and (min-width: 750px) {
  .project-card {
    position: relative;
    display: grid;
    gap: 10px;
    grid-template-columns: repeat(12, 1fr);
    -webkit-box-align: center;
    align-items: center;
    margin-bottom: 75px;
  }
  .project-card .card-content {
    grid-column: 1 / 9;
    position: relative;
    grid-area: 1 / 1 / -1 / 9;
  }
  .project-card:nth-of-type(2n + 1) .card-content {
    grid-column: 5 / -1;
    text-align: right;
  }
  .project-image {
    grid-area: 1 / 6 / -1 / -1;
    position: relative;
    z-index: 1;
  }
  .project-card:nth-of-type(2n + 1) .project-image {
    grid-column: 1 / 8;
  }
}
</style>
