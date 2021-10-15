<template>
  <div class="home_enterprise">
    <b-container>
      <TitleSection :title="Title" :subTitle="subTitle" />
      <div class="d-flex flex-wrap py-4">
        <div
          v-for="(enterprise, index) in Enterprises"
          :key="index"
          class="enterprises_image px-4"
        >
          <img
            :src="enterprise.url"
            alt="Enterprises Image"
            class="enterprise_img mx-auto"
          />
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import TitleSection from "../../../components/Title_Section";
import { Enterprise } from "./Data";
export default {
  name: "Contact",
  data: function () {
    return {
      Title: Enterprise.title,
      Enterprises: Enterprise.lists,
    };
  },
  components: {
    TitleSection,
  },
};
</script>

<style scoped>
.enterprises_image {
  width: 20%;
  margin: 0 auto 40px;
}
.enterprise_img {
  width: 100%;
  height: 80px;
  object-fit: contain;
}
</style>
