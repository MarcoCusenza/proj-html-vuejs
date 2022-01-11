<template>
  <div class="header-top">
    <div class="container">
      <div class="open-hours">
        <i class="fas fa-clock"></i>
        <span>Open Hours: Mon - Sat - {{ openHour }} - {{ closeHour }}</span>
      </div>
      <div class="contacts">
        <a class="phone" href="#">
          <i class="fas fa-phone-alt"></i>
          <span>{{ phone }}</span>
        </a>
        <a class="mail" href="#">
          <i class="fas fa-envelope"></i>
          <span>{{ mail }}</span>
        </a>
        <a class="fb" href="#">
          <i class="fab fa-facebook-f"></i>
        </a>
        <a class="twitter" href="#">
          <i class="fab fa-twitter"></i>
        </a>
        <a class="linkedin" href="#">
          <i class="fab fa-linkedin-in"></i>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderTop",
  data() {
    return {
      openHour: "9:00",
      closeHour: "18:00",
      phone: "+1 (305) 1234-5678",
      mail: "hello@example.com",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.header-top {
  background-color: $bg-dark;
  color: $text-light-low-contrast;
  font-size: .8125rem;
  padding: 15px 0;

  .container {
    display: flex;
    justify-content: space-between;

    .open-hours {
      .fa-clock {
        margin-right: 8px;
      }
    }

    .contacts {
      .phone {
        .fa-phone-alt {
          margin-right: 7px;
        }
      }
      .mail {
        .fa-envelope {
          margin-right: 7px;
        }
      }
      & > * {
        margin-left: 30px;
      }
    }
  }
}
</style>