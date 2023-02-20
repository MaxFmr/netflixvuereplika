<template>
  <section class="w-[100%] border flex flex-col flex-wrap overflow-scroll">
    <h2>{{ movie.category }}</h2>
    <div class="flex">
      <div v-for="image in images" class="h-[200px] w-[300px]">
        <img :src="image" alt="" height="300" width="300" />
      </div>
    </div>
  </section>
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
    return { images: this.movie.images };
  },
};
</script>
