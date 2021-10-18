<template>
  <div class="header_body" :class="{ header_fixed: position }">
    <b-container class="d-flex justify-content-between align-items-center">
      <div class="box_img">
        <a href="/">
          <img
            src="https://cls.vn/images/configs/2021/07/14/logo-cls-072021-01-451.png"
            alt="logo"
            class="header_img"
            :class="{ img_fixed: position }"
        /></a>
      </div>
      <div>
        <ul class="d-flex menu p-0">
          <li>VỀ CHÚNG TÔI</li>
          <li class="drop_downs">
            GIẢI PHÁP E-LEARNING
            <ul class="sub_menu">
              <li class="sub_item">Hệ thống e-learning cho doanh nghiệp</li>
              <li class="sub_item">Hệ thống e-learning cho trường học</li>
            </ul>
          </li>

          <li>SỐ HOÁ BÀI GIẢNG</li>
          <li>KHÁCH HÀNG</li>
          <li class="drop_downs">
            TIN TỨC
            <ul class="sub_menu">
              <li class="sub_item">Bài viết E-learning</li>
              <li class="sub_item">Báo chí nói gì về CLS</li>
            </ul>
          </li>

          <li>BÁO GIÁ</li>
        </ul>
      </div>
      <div>
        <a href="" class="btn btn-outline-orange">Tư vấn miễn phí</a>
        <a href="" class="btn btn-orange">Dùng thử</a>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../assets/css/base.css";

export default {
  name: "HeaderBody",
  data: function () {
    return {
      position: false,
    };
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.scrollY > 50) {
        this.position = true;
      } else {
        this.position = false;
      }
    },
  },
};
</script>

<style scoped>
.header_body {
  position: relative;
  background-color: #fff;
  font-size: 12px;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 4px 5px;
  z-index: 1;
  transition: all 0.3s;
}
.header_fixed {
  position: fixed;
  width: 100%;
  top: 0;
  z-index: 999;
}
.header_img {
  width: 100%;
  transition: all 0.3s;
}
.box_img {
  flex-shrink: 0;
  width: 115px;
}
.img_fixed {
  width: 80px;
}
.menu {
  display: flex;
  justify-content: space-around;
  align-items: center;
  margin: 0;
}
.menu > li {
  cursor: pointer;
  color: var(--main-color);
  list-style-type: none;
  font-weight: 600;
  padding: 30px 0;
  position: relative;
  margin: 0 10px;
}
.menu > li:hover {
  color: var(--hover-color);
}
.menu > li:hover::before {
  position: absolute;
  content: "";
  height: 2px;
  width: 100%;
  bottom: 0;
  background: #0040a0;
}
.drop_downs {
  position: relative;
}
.drop_downs:hover .sub_menu {
  display: block;
}
.sub_menu {
  display: none;
  padding: 0;
  list-style: none;
  position: absolute;
  top: 87px;
  left: 0;
  background: rgba(40, 52, 84, 0.9);
  min-width: 250px;
  box-shadow: 0 0 30px 1px rgb(0, 0, 0, 15%);
  z-index: 99;
  border-top: 3px solid var(--hover-color);
  transform-origin: top;
  animation: showSubMenu ease 0.2s;
}
.sub_menu::before {
  position: absolute;
  content: "";
  background: transparent;
  width: 100%;
  height: 25px;
  top: -25px;
  left: 0;
}
.sub_menu::after {
  position: absolute;
  content: "";
  border-width: 8px 8px;
  border-style: solid;
  border-color: transparent transparent var(--hover-color) transparent;
  left: 5%;
  top: -32%;
  z-index: -1;
}
.sub_item {
  color: var(--white-color);
  padding: 5px 10px;
  border-bottom: 1px solid var(--hover-color);
}
@keyframes showSubMenu {
  from {
    opacity: 0;
    transform: scaleY(0);
  }
  to {
    opacity: 1;
    transform: scaleY(1);
  }
}
</style>
