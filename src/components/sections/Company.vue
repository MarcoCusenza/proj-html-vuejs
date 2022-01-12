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
import CardSimple from "../commons/CardSimple.vue";
import SectionTitle from "../commons/SectionTitle.vue";

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
        title: "The Company",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga atque dignissimos hic non illum ducimus totam praesentium voluptate magni molestiae impedit ex labore maiores amet alias quasi nobis sapiente?",
      },
      cardsData: {
        card1: {
          logo: "fas fa-award",
          title: "Tradition",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card2: {
          logo: "fas fa-lock",
          title: "Security",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card3: {
          logo: "fas fa-edit",
          title: "Certificate",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card4: {
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
  padding: 100px;
  .container {
    display: grid;
    grid-template-columns: 50% 50%;

    .box {
      .text {
        font-size: 0.875rem;
        color: $text-light-low-contrast;
        margin-top: 20px;
      }

      &:first-of-type{
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