<template>
  <div class="footer-top dark-section">
    <div class="container">
      <div class="box-left">
        <img
          class="logo"
          src="../../assets/img/nexgen-logo.svg"
          alt="Nexgen logo"
        />
        <div class="subtitle">
          A Functional HTML Template for Corporate & Business.
        </div>
        <a class="contact phone" href="#">
          <i class="fas fa-phone-alt"></i>
          <span>+1 (305) 1234-5678</span>
        </a>
        <a class="contact mail" href="#">
          <i class="fas fa-envelope"></i>
          <span>hello@example.com</span>
        </a>
        <a class="contact address" href="#">
          <i class="fas fa-map-marker-alt"></i>
          <span>Main Avenue, 987</span>
        </a>
        <button class="but but-empty">get in touch</button>
      </div>
      <div class="box-right">
        <div class="box-card" v-for="(card, i) in footerData" :key="i">
          <div class="card">
            <h3>{{ card.title }}</h3>
            <div class="voice" v-for="(voice, i) in card.voices" :key="i">
              <i class="fas fa-chevron-right"></i>
              <span>{{ voice }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterTop",
  data() {
    return {
      footerData: {
        card1: {
          title: "About",
          voices: {
            voice01: "The Company",
            voice02: "Institutional",
            voice03: "TSocial & Events",
            voice04: "Innovation",
            voice05: "Environment",
            voice06: "Technology",
          },
        },
        card2: {
          title: "Services",
          voices: {
            voice01: "Audit & Assurance",
            voice02: "Financial & Advisory",
            voice03: "Analytics M&A",
            voice04: "Middle Marketing",
            voice05: "Legal Consulting",
            voice06: "Regulatory Risk",
          },
        },
        card3: {
          title: "Support",
          voices: {
            voice01: "Resposability",
            voice02: "Terms of Use",
            voice03: "About Cookies",
            voice04: "Privacy Policy",
            voice05: "Accessibility",
            voice06: "Information",
          },
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

.footer-top {
  background-color: $bg-darker;
  padding: 120px 0;

  .container {
    display: grid;
    grid-template-columns: 25% 75%;

    .box-left {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      img {
        width: 140px;
      }

      .subtitle {
        font-size: 0.875rem;
        width: 90%;
      }

      .contact{
        span{
          margin-left: 10px;
        }
      }

      button {
        width: 150px;
        color: $text-light;
      }
    }
    .box-right {
      display: flex;
      justify-content: space-between;

      .box-card {
        background-color: #19191f;
        padding: 35px 40px;
        border-radius: 10px;

        h3 {
          font-size: 1.375rem;
          margin-bottom: 15px;
        }

        .voice {
          line-height: 30px;

          span {
            margin-left: 10px;
          }
        }
      }
    }
  }
}
</style>