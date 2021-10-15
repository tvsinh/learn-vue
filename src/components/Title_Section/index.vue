<template>
  <div class="section_header">
    <div class="title_header">
      <h2 class="title_name">{{ title }}</h2>
    </div>
    <p class="sub_title">{{ subTitle }}</p>
  </div>
</template>

<script>
import "../../assets/css/base.css";
export default {
  name: "TitleSection",
  props: {
    title: String,
    subTitle: String,
  },
};
</script>

<style scoped>
.section_header {
  margin-top: 80px;
  margin-bottom: 40px;
}
.title_header {
  position: relative;
  width: 100%;
}
.title_header::before {
  content: "";
  position: absolute;
  left: 0;
  top: 50%;
  height: 0.5px;
  width: 100%;
  background-color: var(--text-color);
  z-index: -1;
}
.title_name {
  font-size: var(--title-section);
  background-color: #fff;
  padding: 0 25px;
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
}
.sub_title {
  font-size: var(--subTitle-section);
  color: var(--main-color);
  width: fit-content;
  margin-left: auto;
  margin-right: auto;
}
.sub_title:hover {
  color: var(--hover-color);
}
</style>
