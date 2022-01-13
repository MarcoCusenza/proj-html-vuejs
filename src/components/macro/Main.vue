<template>
  <main>
    <Consulting />
    <Company />
    <Services />
    <Process />
  </main>
</template>

<script>
import Consulting from "../sections/Consulting.vue";
import Company from "../sections/Company.vue";
import Services from "../sections/Services.vue";
import Process from "../sections/Process.vue";

export default {
  name: "Main",
  components: {
    Consulting,
    Company,
    Services,
    Process,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>