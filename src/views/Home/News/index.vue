<template>
  <div class="home_news">
    <b-container>
      <p>Tin tức mới nhất</p>
      <p>Tin tức mới nhất</p>
      <p>Tin tức mới nhất</p>
      <p>Tin tức mới nhất</p>
      <p>Tin tức mới nhất</p>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import { LatestNews } from "./Data";
export default {
  name: "News",
  data: function () {
    return {
      News: LatestNews,
    };
  },
};
</script>

<style scoped>
.home_news {
  height: 200px;
}
</style>
