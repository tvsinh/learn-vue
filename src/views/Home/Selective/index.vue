<template>
  <div class="home_selective">
    <b-container>
      <TitleSection :title="Title" />
      <div class="d-flex">
        <div
          v-for="(item, index) in Selects"
          :key="index"
          class="d-flex flex-column col-lg-3 align-items-center"
        >
          <img
            :src="item.url"
            alt="image"
            width="60px"
            height="60px"
            class="image_select"
          />
          <h5 class="title_select">{{ item.title }}</h5>
          <p class="text_select">{{ item.text }}</p>
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import TitleSection from "../../../components/Title_Section";
import { Selective } from "./Data";
export default {
  name: "Selective",
  data: function () {
    return {
      Title: Selective.title,
      Selects: Selective.list,
    };
  },
  components: {
    TitleSection,
  },
};
</script>

<style scoped>
.image_select {
  object-fit: contain;
}
.title_select {
  font-size: 18px;
  padding: 14px 0 7px;
  color: var(--main-color);
}
.text_select {
  font-size: var(--subTitle-section);
  text-align: justify;
  font-weight: 300;
  color: var(--description-color);
}
</style>
