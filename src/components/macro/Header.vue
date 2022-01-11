<template>
  <header>
    <HeaderTop />
    <HeaderBot />
  </header>
</template>

<script>
import HeaderTop from "../sections/HeaderTop.vue";
import HeaderBot from "../sections/HeaderBot.vue";

export default {
  name: "Header",
  components:{
    HeaderTop,
    HeaderBot,
  }
};
</script>

<style lang="scss" scoped>
@import '../../assets/style/partials/variables.scss';
</style>