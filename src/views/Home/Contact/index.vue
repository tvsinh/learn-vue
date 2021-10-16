<template>
  <div class="home_contact">
    <b-container class="d-flex contact align-items-center">
      <div class="col-lg-7">
        <img :src="Contact.url" alt="learn image" width="100%" />
      </div>
      <div class="col-lg-5 d-flex flex-column">
        <p class="contact_title m-0 text-center">{{ Contact.titleUp }}</p>
        <p class="contact_title m-0 text-center">{{ Contact.titleDown }}</p>
        <p class="contact_subTitle text-center mb-5">{{ Contact.subTitle }}</p>
        <input
          type="text"
          placeholder="Nhập tên cổng đào tạo của bạn"
          class="input_text mb-3"
        />
        <input type="text" placeholder="Email của bạn" class="input_text" />
        <a href="" class="btn btn-view-all mx-auto mt-3 p-2">BẮT ĐẦU</a>
      </div>
    </b-container>
  </div>
</template>

<script>
import "../../../assets/css/base.css";
import { Contacts } from "./Data";
export default {
  name: "Contact",
  data: function () {
    return {
      Contact: Contacts,
    };
  },
};
</script>

<style scoped>
.home_contact {
  background: #eee url(https://cls.vn/Content/images/bg-form-register.png)
    no-repeat center;
  background-size: cover;
  width: 100%;
  margin-top: 0px;
  height: 490px;
}
.contact {
  height: 490px;
}
.contact_title {
  font-size: 27px;
}
.contact_subTitle {
  font-size: 14px;
  color: var(--main-color);
}
.contact_subTitle:hover {
  font-size: 14px;
  color: var(--hover-color);
}
.input_text {
  border-radius: 30px;
  outline: none;
  border: 1px solid var(--border-color);
  height: 40px;
  font-size: 12px;
  padding-left: 20px;
  position: relative;
}
.input_text:focus {
  border: 1px solid #4f95ff;
}
</style>
