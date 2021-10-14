<template>
  <div class="header_top">
    <b-container class="p-0 d-flex justify-content-between">
      <div class="d-flex">
        <div class="d-flex info mr-2 header_phone">
          <b-icon icon="telephone" class="icon"></b-icon>
          <p class="my-auto">0838392666</p>
        </div>
        <div class="d-flex info mr-2">
          <b-icon icon="envelope" class="icon"></b-icon>
          <p class="my-auto">cloudlearningsystem.cls@gmail.com</p>
        </div>
      </div>
      <div class="d-flex info">
        <b-icon icon="person" class="icon"></b-icon>
        <p class="my-auto">Đăng nhập cổng đào tạo</p>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../assets/css/base.css";
export default {};
</script>

<style scoped>
.header_top {
  background-color: var(--main-color);
  color: var(--white-color);
  font-size: 11px;
  padding: 12px;
}
.info:hover {
  color: var(--hover-color);
}
.info:hover .icon {
  transform: rotate(360deg);
}
.icon {
  cursor: pointer;
  font-size: 14px;
  margin-right: 5px;
  margin-top: auto;
  margin-bottom: auto;
  transition: all 0.3s;
}
.header_phone {
  border-right: 1px solid var(--white-color);
  padding-right: 10px;
}
</style>
