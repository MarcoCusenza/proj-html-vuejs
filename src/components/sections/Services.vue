<template>
  <div class="services light-section">
    <div class="container">
      <SectionTitle class="title" :obj="titleData" />
      <div class="top clearfix">
        <span class="floatleft">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga
          atque dignissimos hic non illum ducimus totam praesentium ex labore
          maiores amet alias quasi nobis sapiente?</span
        >
        <button class="but but-full floatright">see all</button>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";

export default {
  name: "Services",
  components: {
    SectionTitle,
  },
  data() {
    return {
      titleData: {
        titleHeader: "our business areas",
        hbefore: "",
        title: "Excellence in",
        hafter: "Services",
        subtitle: "",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/mixin.scss";

@include button;
@include cardServices;

.services {
  background-color: $bg-lightgreen;
  padding: 140px 0;

  .container {
    .top {
      width: 100%;
      span {
        width: 85%;
      }
    }
  }
}
</style>