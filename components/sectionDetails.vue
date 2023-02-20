<template>
  <h1 class="text-white">{{ category.category }}</h1>
</template>

<script>
import movies from "~~/data/movies.json";

export default {
  data() {
    const category = movies.find(
      (movie) => movie.category === this.$route.params.title
    );
    return {
      category,
    };
  },
  name: "AppSectionDetails",
};
</script>
