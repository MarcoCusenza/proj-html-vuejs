<template>
  <div class="company dark-section">
    <div class="container">
      <Title :obj="titleData" />
    </div>
  </div>
</template>

<script>
import Title from "../commons/SectionTitle.vue";

export default {
  name: "Services",
  components: {
    Title,
  },
  data() {
    return {
      titleData: {
        titleHeader: "our business areas",
        title: "Excellence in Services",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga atque dignissimos hic non illum ducimus totam praesentium voluptate magni molestiae impedit ex labore maiores amet alias quasi nobis sapiente?",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>