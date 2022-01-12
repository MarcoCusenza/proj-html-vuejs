<template>
  <div class="company dark-section">
    <div class="container">
      <div class="box">
        <SectionTitle :obj="titleData" />
        <div class="text">
          Tempore sapiente nemo temporibus aperiam error at. Voluptas, libero.
          A, debitis reprehenderit.
        </div>
      </div>
      <div class="box">
        <CardSimple
          v-for="(card, i) in cardsData"
          :key="i"
          :className="'card-company'"
          :obj="card"
        />
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";
import CardSimple from "../commons/CardSimple.vue";

export default {
  name: "Company",
  components: {
    SectionTitle,
    CardSimple,
  },
  data() {
    return {
      titleData: {
        titleHeader: "about the network",
        hbefore: "The",
        title: "Company",
        hafter: "",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga atque dignissimos hic non illum ducimus totam praesentium voluptate magni molestiae impedit ex labore maiores amet alias quasi nobis sapiente?",
        darkness: "dark",
      },
      cardsData: {
        card01: {
          logo: "fas fa-award",
          title: "Tradition",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card02: {
          logo: "fas fa-lock",
          title: "Security",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card03: {
          logo: "fas fa-edit",
          title: "Certificate",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card04: {
          logo: "fas fa-graduation-cap",
          title: "Expertise",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.company {
  padding: 140px 0;
  .container {
    display: grid;
    grid-template-columns: 50% 50%;

    .box {
      .text {
        font-size: $fs-subtitle;
        color: $text-light-low-contrast;
        margin-top: 20px;
      }

      &:first-of-type {
        width: 80%;
      }

      &:last-of-type {
        display: grid;
        grid-template-columns: 50% 50%;
      }
    }
  }
}
</style>