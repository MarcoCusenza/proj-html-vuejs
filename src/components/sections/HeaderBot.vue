<template>
  <div class="header-bot">
    <div class="container">
      <img
        class="logo"
        src="../../assets/img/nexgen-logo.svg"
        alt="Nexgen logo"
      />
      <ul class="navbar">
        <li v-for="(item, i) in nav" :key="i">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderBot",
  data() {
    return {
      nav: [
        "home",
        "about",
        "services",
        "process",
        "team",
        "blog",
        "get in touch",
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";

.header-bot {
  padding: 20px 0;
  background-color: $bg-light;
  color: $text-dark;

  .container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
      width: 110px;
    }

    ul {
      display: flex;
      align-items: center;
      list-style: none;
      text-transform: uppercase;

      li {
        margin: 0 15px;
        font-size: .93rem;
        font-weight: 500;

        &:last-of-type {
          background-color: $primary;
          color: $text-light;
          padding: 10px 20px;
          border-radius: 4px;
        }
      }
    }
  }
}
</style>