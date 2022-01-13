<template>
  <div class="services light-section">
    <div class="container">
      <SectionTitle class="title" :obj="titleData" />
      <div class="top clearfix">
        <span class="floatleft">
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga
          atque dignissimos hic non illum ducimus totam praesentium ex labore
          maiores amet hic non totam alias adipisicing elit quasi nobis
          sapiente?</span
        >
        <button class="but but-full floatright">see all</button>
      </div>
      <div class="box">
        <div class="card" v-for="(card, i) in cardsData" :key="i">
          <CardSimple :className="'card-services'" :obj="card" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";
import CardSimple from "../commons/CardSimple.vue";

export default {
  name: "Services",
  components: {
    SectionTitle,
    CardSimple,
  },
  data() {
    return {
      titleData: {
        titleHeader: "our business areas",
        hbefore: "",
        title: "Excellence in",
        hafter: "Services",
        subtitle: "",
        darkness: "light",
      },
      cardsData: {
        card01: {
          logo: "fas fa-network-wired",
          title: "Audit & Assurance",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card02: {
          logo: "fas fa-briefcase",
          title: "Financial Advisory",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card03: {
          logo: "fas fa-poll",
          title: "Analytics and M&A",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card04: {
          logo: "fas fa-plane",
          title: "Middle Marketing",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card05: {
          logo: "fas fa-globe-europe",
          title: "Legal Consulting",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
        card06: {
          logo: "fas fa-inbox",
          title: "Regulatory Risk",
          subtitle: "Lorem ipsum dolor sit amet consectetur adipiscing elit.",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/card.scss";
@import "../../assets/style/mixins/button.scss";

@include button;
@include cardServices;

.services {
  background-color: $bg-lightgreen;
  padding: 120px 0;

  .container {
    .top {
      width: 100%;
      span {
        width: 80%;
        font-size: $fs-subtitle;
      }
    }
    .box {
      display: grid;
      grid-template-columns: 31.3% 31.3% 31.3%;
      column-gap: 3%;
      row-gap: 8%;
      margin-top: 20px;

      .card {
        background-color: $bg-lightest;
        padding: 10px;
        border-radius: 10px;
      }
    }
  }
}
</style>