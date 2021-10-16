<template>
  <div class="item_news m-0 d-flex">
    <div class="box_image">
      <img
        :src="data.url"
        alt="image news"
        width="135px"
        height="100px"
        class="image"
      />
    </div>
    <div class="content">
      <p class="title m-0">{{ data.title }}</p>
      <p class="subTitle m-0">{{ data.subTitle }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ItemNews",
  props: {
    data: Object,
  },
};
</script>

<style scoped>
.item_news {
  width: 100%;
  overflow: hidden;
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.25) 0px 1px 4px;
}
.box_image {
  flex-shrink: 0;
  overflow: hidden;
  border-radius: 5px;
  position: relative;
}
.box_image::before {
  position: absolute;
  content: "";
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.1);
}
.box_image:hover .image {
  transform: scale(1.1);
}
.image:hover {
  transform: scale(1.1);
}
.image {
  object-fit: cover;
  transition: all 0.1s cubic-bezier(0.47, 0, 0.745, 0.715);
}
.content {
  flex: 1;
  padding: 5px;
}
.title {
  font-size: 16px;
  color: var(--main-color);
  font-weight: 500;
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
}
.subTitle {
  font-size: 12px;
  color: var(--description-color);
  display: -webkit-box;
  -webkit-line-clamp: 2;
  -webkit-box-orient: vertical;
  overflow: hidden;
  text-overflow: ellipsis;
  word-break: break-word;
}
</style>
