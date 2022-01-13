<template>
  <div class="card">
    <img :src="require('../../assets/img/' + obj.image)" alt="obj.name" />
    <div class="box-text">
      <h3 class="name">{{ obj.name }}</h3>
      <div class="role">{{ obj.role }}</div>
      <div class="social">
        <div class="box-logo">
          <a :href="obj.fb" class="fb"><i class="fab fa-facebook-f"></i></a>
        </div>
        <div class="box-logo">
          <a :href="obj.twi" class="twi"><i class="fab fa-twitter"></i></a>
        </div>
        <div class="box-logo">
          <a :href="obj.lin" class="lin"><i class="fab fa-linkedin-in"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CardTeam",
  props: {
    obj: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.card {
  display: grid;
  grid-template-columns: 40% 60%;
  img {
    width: 100px;
    border-radius: 5px;
  }
  .name {
    font-size: 22px;
  }
  .role {
    text-transform: uppercase;
    font-size: 14px;
    margin-top: 10px;
  }
  .social {
    display: flex;
    margin-top: 20px ;

    .box-logo {
      height: 35px;
      width: 35px;
      background-color: $primary-highlight;
      margin-right: 5px;
      border-radius: 50%;
      text-align: center;
      line-height: 35px;

      a {
        color: $primary;
        font-size: 15px;
      }
    }
  }
}
</style>