<template>
  <main>
    <Consulting />
  </main>
</template>

<script>
import Consulting from "../sections/Consulting.vue";

export default {
  name: "Main",
  components: {
    Consulting,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>