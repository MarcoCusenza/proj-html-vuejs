<template>
  <div class="footer-bot dark-section">
    <div class="container">
      <div class="left">
        Enjoy the low price. We are tracking any intention of piracy.
      </div>

      <div class="right">
        &copy; 2020 NEXGEN is Proudly Powered by <a href="#">Codings</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterBot",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.footer-bot {
  background-color: $bg-darkest;

  .container {
    display: flex;
    justify-content: space-between;
    font-size: 14px;
    padding: 30px 0;

    a{
      color: $primary;
    }
  }
}
</style>