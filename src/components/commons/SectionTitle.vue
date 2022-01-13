<template>
  <div class="title-box">
    <h5 class="title-header">{{ obj.titleHeader }}</h5>
    <div class="title">
      <h2 class="hbefore" :class="obj.darkness" v-if="obj.hbefore">
        {{ obj.hbefore }}
      </h2>
      <h2 class="middle">
        <span class="mleft" v-if="obj.hbefore"></span>
        {{ obj.title }}
        <span class="mright" v-if="obj.hafter"></span>
      </h2>
      <h2 class="hafter" :class="obj.darkness" v-if="obj.hafter">
        {{ obj.hafter }}
      </h2>
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
    font-size: $fs-title-header;
  }
  .title {
    display: flex;
    h2 {
      font-size: $fs-title;
      font-weight: 800;
      margin: 20px 0;

      &.middle{
        .mleft{
          margin-left: 10px;
        }
        .mright{
          margin-right: 10px;
        }
      }

      &.hbefore,
      &.hafter {
        background-color: $primary-highlight;
        padding: 0 12px;

        &.light {
          color: $primary;
        }
      }
    }
  }
  .subtitle {
    font-size: $fs-subtitle;
  }
}
</style>