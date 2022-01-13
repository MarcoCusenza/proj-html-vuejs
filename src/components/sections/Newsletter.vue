<template>
  <div class="newsletter dark-section">
    <div class="container">
      <div class="box-left">
        <SectionTitle :obj="titleData" />
      </div>
      <div class="box-right">
        <form action="">
          <input type="text" placeholder="Name" />
          <input type="text" placeholder="Email" />
          <button class="but but-full">subcribe</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";

export default {
  name: "Company",
  components: {
    SectionTitle,
  },
  data() {
    return {
      titleData: {
        titleHeader: "newsletter",
        hbefore: "Know",
        title: "First",
        hafter: "",
        subtitle:
          "Lorem, ipsum dolor sit amet consectetur illum ducimus totam praesentium voluptate magni.",
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
@import "../../assets/style/mixins/button.scss";

@include button;

.newsletter {
  padding: 140px 0;
  background-image: url(../../assets/img/bg-1.jpg);
  background-position: center;
  background-size: cover;

  .container {
    max-width: 850px;
    min-width: 850px;
    display: grid;
    grid-template-columns: 50% 50%;

    .box-left {
      width: 90%;
    }

    .box-right {
      form {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        input {
          padding: 10px;
          border: 2px solid transparent;
          border-radius: 4px;
          font-size: 14px;
          font-family: inherit;
          background-color: $bg-input;

          &:focus {
            outline: none;
            border: 2px solid $primary;
          }
        }

        button {
          width: 120px;
        }

        * {
          margin-bottom: 20px;
        }
      }
    }
  }
}
</style>