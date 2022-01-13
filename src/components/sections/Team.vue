<template>
  <div class="team dark-section">
    <div class="container">
      <div class="box-left">
        <div class="title">
          <SectionTitle :obj="titleData" />
        </div>
        <div class="box-card">
          <div class="card" v-for="(card, i) in cardsData" :key="i">
            <CardTeam :obj="card" />
          </div>
        </div>
      </div>
      <div class="box-right">
        <h3>President Speech</h3>
        <p>
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Doloremque
          odit tempora ea nostrum perferendis.
        </p>
        <p>
          Recusandae inventore vitae, minus rerum labore modi commodi facilis ab
          praesentium deleniti totam optio! Recusandae.
        </p>
        <p>
          Atque repellat quibusdam numquam similique magnam cupiditate officiis
          quidem.
        </p>
        <p>T. Johnson</p>
        <i class="fas fa-quote-right"></i>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";
import CardTeam from "../commons/CardTeam.vue";

export default {
  name: "Team",
  components: {
    SectionTitle,
    CardTeam,
  },
  data() {
    return {
      titleData: {
        titleHeader: "we like what we do",
        hbefore: "Team",
        title: "of Experts",
        hafter: "",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur adipisicing elit. Praesentium voluptate labore maiores amet alias quasi nobis sapiente.",
        darkness: "dark",
      },
      cardsData: {
        card01: {
          image: "team-1.jpg",
          name: "David Cooper",
          role: "cto & co-founder",
          fb: "#",
          twi: "#",
          lin: "#",
        },
        card02: {
          image: "team-3.jpg",
          name: "Oliver Jones",
          role: "chief procurement",
          fb: "#",
          twi: "#",
          lin: "#",
        },
        card03: {
          image: "team-2.jpg",
          name: "Emma Lopez",
          role: "chief marketing",
          fb: "#",
          twi: "#",
          lin: "#",
        },
        card04: {
          image: "team-4.jpg",
          name: "T. Johnson",
          role: "ceo & president",
          fb: "#",
          twi: "#",
          lin: "#",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.team {
  padding: 120px 0 50px 0;
  .container {
    display: grid;
    grid-template-columns: 68% 32%;

    .box-left {
      .title {
        width: 80%;
      }
      .box-card {
        display: grid;
        grid-template-columns: 50% 50%;
        padding: 30px 0;

        .card {
          margin: 10px 0;
        }
      }
    }
    .box-right {
      height: 80%;
      margin-top: 20%;
      background-color: $primary;
      border-radius: 5px;
      padding: 30px;
      position: relative;

      h3 {
        font-size: 22px;
      }

      p {
        margin-top: 30px;
        font-size: $fs-subtitle;
        font-weight: 500;

        &:last-of-type {
          margin-top: 20px;
          font-weight: 700;
          font-size: 16px;
        }
      }

      .fa-quote-right {
        font-size: 22px;
        color: $primary-dark;
        position: absolute;
        right: 30px;
        bottom: 40px;
      }
    }
  }
}
</style>