<template>
  <ul class="navbar">
    <li v-for="(item, i) in nav" :key="i">
      <a href="#">{{ item }}</a>
    </li>
  </ul>
</template>

<script>
export default {
  name: "Navbar",
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

ul {
  display: flex;
  align-items: center;
  list-style: none;
  text-transform: uppercase;

  li {
    margin: 0 15px;
    font-size: 0.9375rem;
    font-weight: 500;

    &:last-of-type {
      background-color: $primary;
      color: $text-light;
      padding: 10px 20px;
      border-radius: 4px;
      margin-right: 0;
    }
  }
}
</style>