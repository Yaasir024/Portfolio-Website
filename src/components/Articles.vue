<script setup>
import { ref, reactive } from "vue";
import { useApiStore } from "@/stores/api";

/*
Use Store 
*/
const apistore = useApiStore();
</script>

<template>
  <section class="articles-section">
    <div class="articles-container">
      <ul class="articles-grid">
        <li
          class="article-card"
          v-for="(post, index) in apistore.posts"
          :key="index"
        >
          <div class="article-inner">
            <div class="header">
              <p class="date">{{ post.dateAdded }}</p>
              <h3 class="title">
                <a
                  :href="`https://teckierite.hashnode.dev/${post.slug}`"
                  target="_blank"
                  >{{ post.title }}</a
                >
              </h3>
              <p class="excerpt">
                {{ post.brief }}
              </p>
            </div>
            <div class="footer">
              <a
                :href="`https://teckierite.hashnode.dev/${post.slug}`"
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
                >
                  <title>Article Link</title>
                  <path
                    d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"
                  ></path>
                  <polyline points="15 3 21 3 21 9"></polyline>
                  <line x1="10" y1="14" x2="21" y2="3"></line>
                </svg>
              </a>
              <a
                href="https://teckierite.hashnode.dev/"
                aria-label="External Link"
                class="external"
                rel="noopener noreferrer"
                target="_blank"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 512 512"
                  fill="currentColor"
                  stroke="currentColor"
                >
                  <title>Blog</title>
                  <path
                    d="M35.19 171.1C-11.72 217.1-11.72 294 35.19 340.9L171.1 476.8C217.1 523.7 294 523.7 340.9 476.8L476.8 340.9C523.7 294 523.7 217.1 476.8 171.1L340.9 35.19C294-11.72 217.1-11.72 171.1 35.19L35.19 171.1zM315.5 315.5C282.6 348.3 229.4 348.3 196.6 315.5C163.7 282.6 163.7 229.4 196.6 196.6C229.4 163.7 282.6 163.7 315.5 196.6C348.3 229.4 348.3 282.6 315.5 315.5z"
                  />
                </svg>
              </a>
            </div>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.articles-section {
  min-height: 100vh;
  width: 100%;
}
.articles-grid {
  list-style: none;
  padding: 0;
  margin-top: 20px;
  display: flex;
  flex-wrap: wrap;
}
.article-card {
  width: 50%;
  padding: 20px;
}
.article-inner {
  background: var(--color-background-soft);

  border-radius: 6px;
  padding: 30px 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  transition: all 0.3s ease;
  min-height: 60px;
}
.article-inner:hover {
  transform: scale(1.02);
}
.date {
  margin-bottom: 10px;
}
.title {
  font-size: 24px;
  font-weight: 700;
  margin-bottom: 15px;
}
.title a {
  font-weight: 700;
}
.footer {
  display: flex;
  align-items: center;
  justify-content: end;
}
.footer a {
  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  padding: 10px;
  cursor: pointer;
}
.footer a svg {
  width: 20px;
  height: 20px;
}
@media only screen and (max-width: 1150px) {
  .articles-container {
    /* max-width: 820px;
    margin: 0 auto; */
    padding: 0 25px;
  }
  .article-card{
    width: 33.33%;
    padding: 6px;
  }
}
@media only screen and (max-width: 850px) {
  .article-card{
    width: 50%;
  }
}
@media only screen and (max-width: 600px) {
  .article-card{
    width: 100%;
  }
}
</style>
