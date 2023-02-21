<template>
  <!-- Header -->
  <app-header></app-header>

  <section
    v-for="movie in movies"
    :movie="movie"
    :key="movie.category"
    class="bg-black ml-2"
  >
    <app-section :movie="movie"></app-section>
  </section>
</template>

<script>
import AppHeader from "../components/header.vue";
import AppSection from "../components/section.vue";
import movies from "../data/movies.json";
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
