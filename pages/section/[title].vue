<template>
  <sectionDetails :category="category"></sectionDetails>
</template>
<script>
import sectionDetails from "~~/components/sectionDetails.vue";

export default {
  data() {
    return {
      category: this.$route.params.title,
    };
  },
  components: {
    sectionDetails,
  },
};
</script>
