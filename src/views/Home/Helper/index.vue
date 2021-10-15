<template>
  <div class="home_helper">
    <b-container>
      <TitleSection :title="Title" :subTitle="subTitle" />
      <div class="">
        <b-carousel
          id="carousel-1"
          v-model="slide"
          :interval="1000"
          fade="true"
          controls
          no-hover-pause="true"
        >
          <b-carousel-slide
            v-for="(person, index) in Persons"
            :key="index"
            class="carousel_item"
          >
            <div class="person_info">
              <p>{{ person.name }}</p>
              <p>{{ person.role }}</p>
              <p>{{ person.description }}</p>
            </div>
            <div class="person_img">
              <img
                class="img-fluid image_item"
                :src="person.url"
                alt="image slot"
                width="100"
                height="200"
              />
            </div>
          </b-carousel-slide>
        </b-carousel>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import TitleSection from "../../../components/Title_Section";
import { Helper } from "./Data";
export default {
  name: "Helper",
  data: function () {
    return {
      Title: Helper.title,
      subTitle: Helper.subTitle,
      Persons: Helper.lists,
    };
  },
  components: {
    TitleSection,
  },
};
</script>

<style scoped>
.home_helper {
  display: block;
}
.carousel_item {
  position: relative;
  height: 300px;
}
.person_img {
  object-fit: contain;
}
.person_img::after {
  position: absolute;
  content: "";
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #e2eefa;
  border-radius: 50%;
  text-align: center;
  width: 310px;
  height: 310px;
  z-index: -1;
}
.image_item {
  position: absolute;
  right: 20%;
  bottom: 0;
  width: 120px;
  height: 250px;
}
</style>
