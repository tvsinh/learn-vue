<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="3000"
      no-hover-pause="true"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            src="https://cls.vn/images/banners/2021/10/02/cover-web-67.jpg?w=1900"
            alt="image slot"
          />
        </template>
      </b-carousel-slide>
      <b-carousel-slide>
        <template #img>
          <img
            class="d-block img-fluid w-100"
            src="	https://cls.vn/images/banners/2021/07/14/banner-web-bao-boi-330.jpg?w=1900"
            alt="image slot"
          />
        </template>
      </b-carousel-slide>
    </b-carousel>
  </div>
</template>

<script>
export default {
  data() {
    return {
      slide: 0,
    };
  },
  methods: {
    onSlideStart() {},
    onSlideEnd() {},
  },
};
</script>
