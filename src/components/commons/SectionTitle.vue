<template>
  <div class="title-box">
    <h5>{{ obj.titleHeader }}</h5>
    <div class="title">
      <h2 class="hbefore" v-if="obj.hbefore">{{ obj.hbefore }}</h2>
      <h2 class="middle">{{ obj.title }}</h2>
      <h2 class="hafter" v-if="obj.hafter">{{ obj.hafter }}</h2>
    </div>
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
.title-box {
  h5 {
    text-transform: uppercase;
    color: $primary-light;
    font-size: 0.8rem;
  }
  .title {
    display: flex;
    h2 {
      font-size: 2.5rem;
      font-weight: 800;
      margin: 20px 0;
    }

    .middle {
      &:before,
      &:after {
        content: "\00A0";
      }
    }

    .hbefore,
    .hafter {
      background-color: $primary-highlight;
      padding: 0 12px;
    }
  }
  .subtitle {
    font-size: 0.875rem;
  }
}
</style>