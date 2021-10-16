<template>
  <div class="home_story">
    <b-container>
      <TitleSection :title="Title" :subTitle="subTitle" />
      <div class="d-flex flex-wrap">
        <div
          v-for="(item, index) in Storys"
          :key="index"
          class="d-flex flex-column col-lg-4 align-items-center"
        >
          <div class="item_root">
            <div class="item_img">
              <img
                :src="item.url"
                alt="image"
                width="100%"
                height="200px"
                class="image"
              />
            </div>
            <div class="item_content">
              <h5 class="mb-2 item_title">
                {{ item.title }}
              </h5>
              <p class="item_text mb-2">{{ item.text }}</p>
              <p class="text_detail mb-0">Xem chi tiết</p>
            </div>
          </div>
        </div>
      </div>
      <div class="text-center mt-4 mb-4">
        <a href="" class="btn btn-view-all">Xem tất cả</a>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import TitleSection from "../../../components/Title_Section";
import { Story } from "./Data";
export default {
  name: "Story",
  data: function () {
    return {
      Title: Story.title,
      subTitle: Story.subTitle,
      Storys: Story.lists,
    };
  },
  components: {
    TitleSection,
  },
};
</script>

<style scoped>
.home_story {
  display: block;
  margin-bottom: -20px;
}
.item_root {
  box-shadow: rgba(0, 0, 0, 0.1) 0px 2px 4px;
  border-radius: 5px;
  overflow: hidden;
  margin-bottom: 20px;
  transition: all 0.3s;
}
.item_root:hover {
  box-shadow: rgb(0, 0, 0, 0.15) 0 15px 15px;
  transform: translateY(-5px);
}
.item_img {
  cursor: pointer;
  position: relative;
  overflow: hidden;
}
.image {
  object-fit: cover;
}
.item_content {
  padding: 12px;
}
.item_title {
  cursor: pointer;
  color: var(--main-color);
  font-size: 15px;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
}
.item_text {
  color: var(--description-color);
  font-size: 12px;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
}
.text_detail {
  font-size: 12px;
  cursor: pointer;
  text-align: right;
  color: var(--description-color);
}
.text_detail:hover {
  color: var(--main-color);
}
.item_img::before {
  left: 0;
  top: 0;
  position: absolute;
  content: "";
  background: rgba(0, 0, 0, 0.1);
  height: 100%;
  width: 100%;
}
</style>
