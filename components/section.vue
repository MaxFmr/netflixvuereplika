<template>
  <div>{{ movie.category }}</div>
  <div v-for="image in images">
    <img :src="image" alt="" />
  </div>
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
