<template>
  <h1 class="text-white">{{ category.category }}</h1>
  <section class="" :movie="movie">
    <div class="flex flex-nowrap overflow-y-scroll">
      <div v-for="image in category.images" class="flex flex-shrink-0">
        <img
          :src="image"
          alt=""
          height="200"
          width="300"
          class="object-cover"
        />
      </div>
    </div>
  </section>
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
