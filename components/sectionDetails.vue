<template>
  <h1 class="text-white ml-5">{{ category.category }}</h1>

  <section
    class="w-[100vw] h-[100vh] flex flex-wrap ml-5 justify-center"
    :movie="movie"
  >
    <div v-for="image in category.images" class="h-[170px] w-[300px] m-1">
      <img :src="image" alt="" height="200" width="300" class="object-cover" />
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
      linkTo: `/section/${this.$route.params.title}/${movies[2].category}`,
    };
  },
  name: "AppSectionDetails",
};
</script>
