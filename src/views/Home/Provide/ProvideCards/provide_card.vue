<template>
  <div id="provide-card">
    <div class="provide_card mt-3">
      <img
        width="100%"
        height="150"
        :src="cardData.url"
        alt="video"
        class="img_video"
      />
      <b-icon icon="play-circle" class="icon_play"></b-icon>
      <div class="">
        <h5 class="mt-2 mb-3 card_title">
          {{ cardData.title }}
        </h5>
      </div>
    </div>
  </div>
</template>

<script>
import "../../../../assets/css/base.css";

export default {
  name: "ProvideCard",
  props: ["cardData"],
};
</script>

<style scoped>
.provide_card {
  padding: 10px;
  cursor: pointer;
  border-radius: 5px;
  margin-bottom: 15px;
  box-shadow: rgba(0, 0, 0, 0.25) 0px 4px 4px;
}
.provide_card:hover .icon_play {
  color: var(--hover-color);
}
.card_title {
  font-size: 14px;
  font-weight: 600;
  color: var(--main-color);
}
.img_video {
  position: relative;
}
.icon_play {
  position: absolute;
  font-size: 40px;
  z-index: 10;
  color: #fff;
  top: 30%;
  left: 50%;
  transform: translateX(-50%);
}
</style>
