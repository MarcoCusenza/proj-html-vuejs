<template>
  <div class="news light-section">
    <div class="container">
      <SectionTitle class="title" :obj="titleData" />
      <div class="top">
        <span>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam, fuga.</span
        >
        <button class="but but-full">see all</button>
      </div>
      <div class="bottom">
        <div class="card first">
          <h3>Increasing creativity is possible for everyone</h3>
        </div>
        <div class="card second">
          <h3>Because market research is part of the business plan</h3>
        </div>
        <div class="card third">
          <h3>Working from home is now a trend</h3>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "../commons/SectionTitle.vue";

export default {
  name: "Services",
  components: {
    SectionTitle,
  },
  data() {
    return {
      titleData: {
        titleHeader: "our editorial content",
        hbefore: "",
        title: "Latest",
        hafter: "News",
        subtitle: "",
        darkness: "light",
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/partials/variables.scss";
@import "../../assets/style/mixins/button.scss";

@include button;

.news {
  background-color: $bg-lightest;
  padding: 120px 0;

  .container {
    .top {
      display: flex;
      justify-content: space-between;
      align-items:flex-end;
      margin-top: -15px;

      span {
        width: 80%;
        font-size: $fs-subtitle;
      }
    }
    .bottom {
      display: grid;
      grid-template-columns: 33.3% 33.3% 33.3%;
      margin-top: 40px;

      .card {
        aspect-ratio: 1;
        border-radius: 10px;
        position: relative;
        text-align: center;
        background-position: center;
        background-size: cover;

        h3{
          width: 80%;
          color: $text-light;
          font-size: 21px;


          position: absolute;
          left: 50%;
          transform: translate(-50%, 0);
          bottom: 30px;
        }
        
      }

      .first{
        margin-right: 20px;
        background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../../assets/img/news-1.jpg");
      }

      .second{
        margin: 0 10px;
        background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../../assets/img/news-2.jpg");
      }

      .third{
        margin-left: 20px;
        background-image: linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)), url("../../assets/img/news-3.jpg");
      }
    }
  }
}
</style>