<template>
  <div class="consulting">
    <div class="container">
      <div class="box-form">
        <h4>fusions & acquisitions</h4>
        <h1>Insurance Consulting</h1>
        <FormConsulting />
      </div>
    </div>
  </div>
</template>

<script>
import FormConsulting from "../commons/FormConsulting.vue";

export default {
  name: "Consulting",
  components: {
    FormConsulting,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.consulting {
  height: 850px;
  background-image: url("../../assets/img/bg-6.jpg");
  background-position: bottom;
  background-size: cover;
  position: relative;

  .container {
    .box-form {
      width: 500px;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(0, -50%);

      h4 {
        text-transform: uppercase;
        font-weight: 500;
        color: $primary-light;
      }
      h1 {
        font-size: 65px;
        font-weight: 900;
        line-height: 70px;
        color: $text-dark;
        margin: 10px 0 30px 0;
      }
    }
  }
}
</style>