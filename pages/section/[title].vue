<template>
  <AppHeader></AppHeader>
  <sectionDetails></sectionDetails>
</template>
<script>
import sectionDetails from "~~/components/sectionDetails.vue";
import AppHeader from "~~/components/header.vue";

export default {
  components: {
    sectionDetails,
    AppHeader,
  },
};
</script>
