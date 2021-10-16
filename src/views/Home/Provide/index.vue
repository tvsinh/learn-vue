<template>
  <b-container id="provide">
    <b-nav tabs align="center mt-5">
      <b-nav-item @click="activeMenu(active)" :active="active" class="nav_item">
        Giải pháp E-learninb
      </b-nav-item>
      <b-nav-item
        @click="activeMenu(active)"
        :active="!active"
        class="ml-3 nav_item"
        >Số hoá nội dung</b-nav-item
      >
    </b-nav>
    <div
      v-if="active"
      class="d-flex flex-wrap mt-4 justify-content-center provide_list"
    >
      <p class="heading">{{ Heading }}</p>
      <div
        v-for="(item, index) in List"
        :key="index"
        class="col-lg-6 provide_item"
      >
        <ProvideItem :listData="item" />
      </div>
    </div>
    <div v-else class="d-flex flex-wrap justify-content-between">
      <div v-for="(card, index) in Cards" :key="index" class="col-lg-4">
        <ProvideCard :cardData="card" />
      </div>
    </div>
    <div class="text-center mt-4 mb-4">
      <a href="" class="btn btn-view-all">Xem tất cả</a>
    </div>
  </b-container>
</template>

<script>
import { ProvideList } from "./data/provide_list";
import { ProvideCards } from "./data/provide_cards";
import ProvideItem from "./provide_item.vue";
import ProvideCard from "./provide_card.vue";
export default {
  name: "Provide",
  data: function () {
    return {
      active: true,
      Heading: ProvideList.heading,
      List: ProvideList.ListData,
      Cards: ProvideCards,
    };
  },
  methods: {
    activeMenu(active) {
      this.active = !active;
    },
  },
  components: {
    ProvideItem,
    ProvideCard,
  },
};
</script>

<style scoped>
.nav_item {
  border: 1px solid #c4c4c4;
  border-bottom: 0;
  font-size: var(--title-section);
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
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
.provide_list {
  margin: 0 -15px;
}
.provide_item {
  padding: 15px;
}
.heading {
  font-size: 14px;
}
</style>
