<template>
  <div class="card" :class="className">
    <div class="title">
      <i :class="obj.logo" class="icon"></i>
      <h3>{{ obj.title }}</h3>
    </div>
    <div class="subtitle">{{ obj.subtitle }}</div>
  </div>
</template>

<script>
export default {
  name: "CardCompany",
  props: {
    className: String,
    obj: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/mixin.scss";

@include cardCompany;
</style>