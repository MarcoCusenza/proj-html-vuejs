<template>
  <footer>
    <FooterTop />
    <FooterBot />
  </footer>
</template>

<script>
import FooterTop from "../sections/FooterTop.vue";
import FooterBot from "../sections/FooterBot.vue";

export default {
  name: "Footer",
  components:{
    FooterTop,
    FooterBot,
  }
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
</style>