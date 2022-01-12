<template>
  <div class="header-bot">
    <div class="container">
      <img
        class="logo"
        src="../../assets/img/nexgen-logo.svg"
        alt="Nexgen logo"
      />
      <Navbar />
    </div>
  </div>
</template>

<script>
import Navbar from "../commons/Navbar.vue";

export default {
  name: "HeaderBot",
  components:{
    Navbar,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.header-bot {
  background-color: rgba(255, 255, 255, 0);
  color: $text-dark;

  .container {
    width: 1050px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 0;
    position: fixed;
    left: 50%;
    transform: translate(-50%, 0);

    img {
      width: 110px;
    }
  }
}
</style>