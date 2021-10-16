<template>
  <div class="home_helper">
    <b-container>
      <TitleSection :title="Title" :subTitle="subTitle" />
      <div class="">
        <b-carousel
          id="carousel-2"
          v-model="slide"
          :interval="3000"
          controls
          no-hover-pause="true"
        >
          <b-carousel-slide
            v-for="(person, index) in Persons"
            :key="index"
            class="carousel_item"
          >
            <div class="d-flex">
              <div class="person_logo col-lg-1"></div>
              <div class="person_info col-lg-5">
                <p class="person_name">{{ person.name }}</p>
                <p class="person_role">{{ person.role }}</p>
                <p class="person_description">{{ person.description }}</p>
              </div>
              <div class="person_img col-lg-6">
                <img
                  class="img-fluid image_item"
                  :src="person.url"
                  alt="image slot"
                />
              </div>
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

<style>
.carousel-control-prev,
.carousel-control-next {
  opacity: 1;
}
.carousel-control-next-icon,
.carousel-control-prev-icon {
  opacity: 1;
  padding: 15px;
  border-radius: 50%;
  background: var(--main-color);
  background-repeat: no-repeat;
}
.carousel-control-next-icon {
  background-position: 55% 50%;
  background-size: 12px 12px;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='%23fff' width='8' height='8' viewBox='0 0 8 8'%3e%3cpath d='M2.75 0l-1.5 1.5L3.75 4l-2.5 2.5L2.75 8l4-4-4-4z'/%3e%3c/svg%3e");
}

.carousel-control-prev-icon {
  background-position: 45% 50%;
  background-size: 12px 12px;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' fill='%23fff' width='8' height='8' viewBox='0 0 8 8'%3e%3cpath d='M5.25 0l-4 4 4 4 1.5-1.5L4.25 4l2.5-2.5L5.25 0z'/%3e%3c/svg%3e");
}

.home_helper {
  margin-bottom: 45px;
}
.carousel_item {
  position: relative;
  height: 450px;
}
.person_logo {
  background-image: url(https://cls.vn/Content/images/quote.svg);
  background-repeat: no-repeat;
  background-size: 64px 46px;
}
.person_info {
  color: black;
  text-align: left;
  padding-top: 18px;
}
.person_name {
  color: var(--text-color);
  font-size: 18px;
}
.person_role {
  color: var(--description-color);
  font-size: 14px;
}
.person_description {
  color: var(--description-color);
  font-size: 14px;
}
.person_img::after {
  position: absolute;
  content: "";
  width: 310px;
  height: 310px;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  border-radius: 50%;
  background: #e2eefa;
  z-index: -1;
}
.image_item {
  object-fit: contain;
  width: 230px;
  height: 400px;
}
</style>
