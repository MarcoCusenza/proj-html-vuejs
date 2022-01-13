<template>
  <div class="process light-section">
    <div class="container">
      <div class="title-box">
        <h5 class="title-header">{{ titleData.titleHeader }}</h5>
        <div class="title">
          <h2
            class="hbefore"
            :class="titleData.darkness"
            v-if="titleData.hbefore"
          >
            {{ titleData.hbefore }}
          </h2>
          <h2 class="middle">{{ titleData.title }}</h2>
          <h2
            class="hafter"
            :class="titleData.darkness"
            v-if="titleData.hafter"
          >
            {{ titleData.hafter }}
          </h2>
        </div>
        <div class="subtitle">{{ titleData.subtitle }}</div>
      </div>
    </div>
    <div class="timeline">
      <div class="line">
        <div class="line-container">
          <div class="box-number" v-for="(card, i) in cardsData" :key="i">
            <div class="number">
              {{ card.id }}
            </div>
          </div>
        </div>
      </div>
      <div class="box-card">
        <div class="card" v-for="(card, i) in cardsData" :key="i">
          <CardSimple :className="'card-process'" :obj="card" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import CardSimple from "../commons/CardSimple.vue";

export default {
  name: "Process",
  components: {
    CardSimple,
  },
  data() {
    return {
      titleData: {
        titleHeader: "how it works in practice",
        hbefore: "Process",
        title: "Management",
        hafter: "",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur ducimus totam praesentium voluptate ex labore maiores amet alias quasi nobis sapiente.",
        darkness: "light",
      },
      cardsData: {
        card01: {
          id: "01",
          title: "Collection of information",
          subtitle: "Lorem ipsum dolor sit amet consectetur.",
        },
        card02: {
          id: "02",
          title: "Strategic planning",
          subtitle: "Lorem ipsum dolor sit amet consectetur.",
        },
        card03: {
          id: "03",
          title: "Assignment of responsibilities",
          subtitle: "Lorem ipsum dolor sit amet consectetur.",
        },
        card04: {
          id: "04",
          title: "Formatting process",
          subtitle: "Lorem ipsum dolor sit amet consectetur.",
        },
        card05: {
          id: "05",
          title: "Continuity formalization",
          subtitle: "Lorem ipsum dolor sit amet consectetur.",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/card.scss";

@include cardProcess;

.process {
  padding: 140px 0;
  .container {
    .title-box {
      h5 {
        text-transform: uppercase;
        font-size: $fs-title-header;
        text-align: center;
      }
      .title {
        display: flex;
        justify-content: center;
        h2 {
          font-size: $fs-title;
          font-weight: 800;
          margin: 20px 0;

          &.middle {
            &:before,
            &:after {
              content: "\00A0";
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
        width: 70%;
        margin: 0 auto;
        text-align: center;
      }
    }
  }
  .timeline {
    margin: 40px 0;
    .line {
      background-image: linear-gradient(
        $bg-lightest 0 45%,
        #daeced 45% 55%,
        $bg-lightest 55% 100%
      );
      .line-container {
        width: 1400px;
        margin: 0 auto;
        display: flex;
        justify-content: space-around;
        align-items: center;

        .box-number {
          padding: 10px;
          text-align: center;
          position: relative;

          .number {
            width: 40px;
            height: 40px;
            line-height: 39px;
            margin: auto;
            background-color: #daeced;
            border-radius: 50%;
            font-size: 16px;
            font-weight: 700;
            color: $primary;
          }
        }
      }
    }

    .box-card {
      width: 1400px;
      margin: 0 auto;
      display: flex;
      justify-content: space-around;

      .card {
        width: 280px;
      }
    }
  }
}
</style>