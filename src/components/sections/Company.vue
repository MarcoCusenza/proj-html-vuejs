<template>
  <div class="company dark-section">
    <div class="container">
      <div class="box">
        <SectionTitle :obj="titleData" />
        <div class="text">Tempore sapiente nemo temporibus aperiam error at. Voluptas, libero. A, debitis reprehenderit.</div>
      </div>
      <div class="box">
        <CardCompany />
        <CardCompany />
        <CardCompany />
        <CardCompany />
      </div>
    </div>
  </div>
</template>

<script>
import CardCompany from "../commons/CardCompany.vue";
import SectionTitle from "../commons/SectionTitle.vue";

export default {
  name: "Company",
  components: {
    SectionTitle,
    CardCompany,
  },
  data() {
    return {
      titleData: {
        titleHeader: "about the network",
        title: "The Company",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga atque dignissimos hic non illum ducimus totam praesentium voluptate magni molestiae impedit ex labore maiores amet alias quasi nobis sapiente?",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.company {
  padding: 100px;

  .box {
    width: 50%;

    .text{
    font-size: .875rem;
    color: $text-light-low-contrast;
    margin-top: 20px;
  }

    
  }
}
</style>