<template>
  <div class="form-consulting">
    <form>
      <div class="inputs">
        <input type="text" placeholder="Name" />
        <input type="text" placeholder="Email" />
        <input type="text" placeholder="Phone" />
        <select name="more-info" id="more-info">
          <option value="1">
            <span>More Info <i class="fas fa-chevron-down"></i></span>
          </option>
          <option value="1">Info 1</option>
          <option value="2">Info 2</option>
          <option value="3">Info 3</option>
          <option value="4">Info 4</option>
        </select>
      </div>
      <button class="but but-full">get in touch</button>
      <button class="but but-empty">read more</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "FormConsulting",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/button.scss";

@include button;

form {
  .inputs {
    height: 130px;
    display: grid;
    grid-template-columns: 45% 45%;
    grid-template-rows: 40% 40%;
    row-gap: 10%;
    column-gap: 3%;

    input {
      padding: 10px;
      border: 2px solid transparent;
      border-radius: 4px;
      font-size: 14px;
      font-family: inherit;
      background-color: $bg-input;

      &:focus {
        outline: none;
        border: 2px solid $primary;
      }
    }
    select {
      padding: 12px;
      border: none;
      border-radius: 4px;
      font-size: 14px;
      background-color: $bg-input;
      color: $text-grey;
      font-family: inherit;
      cursor: pointer;

      appearance: none;
      -moz-appearance: none;
      -webkit-appearance: none;

      background-image: url("../../assets/img/chevron-down-solid.svg");
      background-repeat: no-repeat;
      background-position: calc(100% - 10px) center;
      background-size: 15px;

      option {
        border: none;
        font-family: inherit;
        background-color: #d5d6d8;
        font-size: 16px;
      }
    }
  }
  button {   
    &:first-of-type {
      margin-right: 15px;
    }
  }
}
</style>