<template>
  <nuxt-link :to="linkTo">
    <section class="w-[100vw] h-[200px] flex flex-col" :movie="movie">
      <h2 class="text-white text-lg font-bold mb-3 mt-3">
        {{ movie.category }}
      </h2>
      <div class="flex flex-nowrap overflow-y-scroll">
        <div v-for="image in images" :kry="image" class="flex flex-shrink-0">
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
  </nuxt-link>
</template>

<script>
export default {
  name: "AppSection",
  props: {
    movie: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      images: this.movie.images,
      linkTo: `/section/${this.movie.category}`,
    };
  },
};
</script>
