<template>
  <main>
    <Consulting />
    <Company />
    <Services />
  </main>
</template>

<script>
import Consulting from "../sections/Consulting.vue";
import Company from "../sections/Company.vue";
import Services from "../sections/Services.vue";

export default {
  name: "Main",
  components: {
    Consulting,
    Company,
    Services,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>