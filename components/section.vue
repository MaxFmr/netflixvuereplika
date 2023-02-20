<template>
  <div>{{ movie.category }}</div>
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
};
</script>
