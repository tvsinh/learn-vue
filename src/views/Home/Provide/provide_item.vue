<template>
  <div id="provide-item">
    <div class="d-flex">
      <img width="95" height="95" :src="listData.url" alt="placeholder" />
      <div class="media_body" :class="{ toggle: show }">
        <h5 class="mt-0 mb-1 media_title" @click="toggle(show)">
          {{ listData.title }}
        </h5>
        <p v-if="!show" class="mb-0 media_text">
          {{ listData.text }}
        </p>
        <p v-else class="mb-0 toggle_text">
          {{ listData.text }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import "../../../assets/css/base.css";

export default {
  name: "ProvideItem",
  props: {
    listData: Object,
  },
  data() {
    return {
      show: false,
    };
  },
  methods: {
    toggle(show) {
      this.show = !show;
    },
  },
};
</script>

<style scoped>
.media_body {
  padding: 1rem;
  margin-left: 1rem;
  border-radius: 5px;
  box-shadow: 0 1px 4px rgb(0, 0, 0, 25%);
  background: #fff;
  height: 80px;
}
.toggle {
  height: auto;
}
.media_title {
  cursor: pointer;
  font-size: 15px;
  color: var(--main-color);
}
.media_text {
  font-size: 12px;
  width: 100%;
  /* text-truncate */
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
}
.toggle_text {
  font-size: 12px;
  width: 100%;
}
</style>
