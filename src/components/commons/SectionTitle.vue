<template>
  <div class="title">
    <h5>{{ obj.titleHeader }}</h5>
    <h2>{{ obj.title }}</h2>
    <div class="subtitle">{{ obj.subtitle }}</div>
  </div>
</template>

<script>
export default {
  name: "SectionTitle",
  props: {
    obj: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
.title {
  h5 {
    text-transform: uppercase;
    color: $primary-light;
    font-size: 0.75rem;
  }
  h2 {
    font-size: 2.5rem;
    font-weight: 800;
    margin: 20px 0;
  }
  .subtitle{
    font-size: .875rem;
    color: $text-light-low-contrast
  }
}
</style>