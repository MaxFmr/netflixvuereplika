<template>
  <!-- Header -->
  <app-header></app-header>

  <!-- Section -->
  <div v-for="movie in movies">
    <app-section :movie="movie"></app-section>
  </div>
</template>

<script>
import AppHeader from "./components/header.vue";
import AppSection from "./components/section.vue";
import movies from "./data/movies.json";
export default {
  name: "App",
  components: {
    AppHeader,
    AppSection,
  },
  data() {
    return {
      movies,
    };
  },
};
</script>
