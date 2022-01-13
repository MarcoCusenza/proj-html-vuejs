<template>
  <div class="card" :class="className">
    <div class="box-title">
      <div class="icons">
        <i :class="obj.logo"></i>
        <i class="fas fa-arrow-right"></i>
      </div>
      <h3 class="title">{{ obj.title }}</h3>
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
@import "../../assets/style/mixins/card.scss";

@include cardCompany;
@include cardServices;
@include cardProcess;
</style>