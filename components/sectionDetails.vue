<template>
  <h1 class="text-white">{{ category }}</h1>
</template>

<script>
export default {
  name: "AppSectionDetails",
  props: {
    category: {
      type: Object,
      required: true,
    },
  },
};
</script>
