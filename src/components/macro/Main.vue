<template>
  <main>
    <Consulting />
    <Company />
  </main>
</template>

<script>
import Consulting from "../sections/Consulting.vue";
import Company from "../sections/Company.vue";

export default {
  name: "Main",
  components: {
    Consulting,
    Company,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>