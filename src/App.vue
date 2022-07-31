<script setup>
import { RouterLink, RouterView } from "vue-router";
import { ref, reactive, onMounted, } from "vue";
import { useApiStore } from "@/stores/api";

/*
Use Store 
*/
const apistore = useApiStore();

onMounted(() => {
  apistore.getPosts()
});
</script>

<template>
  <RouterView />
</template>

<style scoped></style>
