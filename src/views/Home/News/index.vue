<template>
  <div class="home_news">
    <b-container class="d-flex">
      <div class="col-lg-6">
        <div class="d-flex justify-content-between align-items-baseline">
          <p class="header_title">Tin tức mới nhất</p>
          <p class="view_all">Xem tất cả</p>
        </div>
        <div class="left_body">
          <img
            :src="LeftData.url"
            alt="image"
            width="100%"
            height="330px"
            class="left_img"
          />
          <div class="content">
            <p class="title">{{ LeftData.title }}</p>
            <p class="subTitle">{{ LeftData.subTitle }}</p>
          </div>
        </div>
      </div>
      <div class="col-lg-6">
        <b-nav tabs class="d-flex justify-content-between flex-nowrap">
          <b-nav-item
            @click="setPapers(item)"
            :active="papers"
            class="nav_item"
          >
            <span>Báo chí nói về CLS</span>
          </b-nav-item>
          <b-nav-item
            @click="setCustomer(item)"
            :active="customer"
            class="nav_item"
            ><span>Khách hàng</span></b-nav-item
          >
          <b-nav-item @click="setNews(item)" :active="news" class="nav_item"
            ><span>Tin tức</span></b-nav-item
          >
        </b-nav>
        <div class="right_content">
          <div v-if="papers">
            <div
              v-for="(newspaper, index) in newspaperList"
              :key="index"
              class="content_body pb-1"
            >
              <ItemNews :data="newspaper" />
            </div>
          </div>
          <div v-else-if="customer">
            <div
              v-for="(customer, index) in customerList"
              :key="index"
              class="content_body pb-1"
            >
              <ItemNews :data="customer" />
            </div>
          </div>
          <div v-else>
            <div
              v-for="(news, index) in newsList"
              :key="index"
              class="content_body pb-1"
            >
              <ItemNews :data="news" />
            </div>
          </div>
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import { LatestNews } from "./Data";
import ItemNews from "./item_news.vue";
export default {
  name: "News",
  data: function () {
    return {
      papers: false,
      customer: true,
      news: false,
      LeftData: LatestNews.left,
      newspaperList: LatestNews.right.newspapers,
      customerList: LatestNews.right.customers,
      newsList: LatestNews.right.news,
    };
  },
  methods: {
    setPapers() {
      this.papers = true;
      this.customer = false;
      this.news = false;
    },
    setCustomer() {
      this.papers = false;
      this.customer = true;
      this.news = false;
    },
    setNews() {
      this.papers = false;
      this.customer = false;
      this.news = true;
    },
  },
  components: {
    ItemNews,
  },
};
</script>

<style scoped>
.home_news {
  margin-top: 40px;
  margin-bottom: 70px;
}
.header_title {
  font-size: 26px;
}
.view_all {
  font-size: 16px;
  color: var(--main-color);
}
.left_body {
  position: relative;
}
.left_img {
  border-radius: 5px;
  object-fit: cover;
}
.content {
  position: absolute;
  width: 100%;
  bottom: 0;
  padding: 16px;
  color: var(--white-color);
  background-color: rgba(0, 0, 0, 0.5);
}
.title {
  font-size: 17px;
  margin: 0 0 5px;
}
.subTitle {
  font-size: 14px;
  margin: 0;
}
/* right */
.nav_item {
  border: 1px solid #c4c4c4;
  border-bottom: 0;
  font-size: 16px;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
  background-color: #e0e0e0;
}
span {
  padding: 0 20px;
}
.nav-tabs .nav-link {
  border: 0;
  color: var(--text-color);
}
.active {
  color: #0040a0;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
.nav_item .active {
  color: #0040a0;
}
.right_content {
  margin-top: -1px;
  border: 1px solid #ccc;
  border-top: none;
}
.content_body {
  padding: 11px;
}
</style>
