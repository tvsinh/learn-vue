<template>
  <div class="footer">
    <b-container>
      <div class="row">
        <div class="col-lg-4">
          <h4>Hỗ trợ</h4>
          <ul>
            <li>Liên hệ</li>
            <li>Câu hỏi thường gặp</li>
          </ul>
        </div>
        <div class="col-lg-4">
          <h4>Chính sách &amp; Quy định</h4>
          <ul>
            <li>Điều khoản sử dụng và Chính sách bảo mật thông tin</li>
            <li>Hình thức thanh toán</li>
          </ul>
        </div>
        <div class="col-lg-4 mt-0">
          <h4>Ứng dụng di động</h4>
          <div class="row">
            <div class="col-lg-6">
              <img
                src="https://cls.vn/Content/images/logo-icon/apple.svg"
                alt="iOS"
              />
              <img
                src="https://cls.vn/images/configs/2021/09/23/ios-1-959.png"
                class="img_QR"
                alt="CLS E-Learning"
              />
            </div>
            <div class="col-lg-6">
              <img
                src="https://cls.vn/Content/images/logo-icon/andro.svg"
                alt="Android"
              />
              <img
                src="https://cls.vn/images/configs/2021/09/23/android-2-2-457.png"
                class="img_QR"
                alt="CLS E-Learning"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="mt-5 mb-4">
        <div class="row">
          <div class="col">
            <div>
              <h4>Văn phòng <strong>miền Bắc</strong></h4>
              <ul>
                <li>Tầng 16, Khối A, Tòa nhà sông Đà Nam Từ Liêm, Hà Nội</li>
                <li>Điện thoại:0838392666</li>
                <li>Liên hệ hợp tác:&nbsp;0835413999</li>
                <li>Email: cloudlearningsystem.cls@gmail.com</li>
              </ul>
            </div>
          </div>
          <div class="col">
            <div>
              <h4>Văn phòng <strong>miền Trung</strong></h4>
              <ul>
                <li>
                  Tầng 9, Công viên phần mềm Đà Nẵng, 02 Quang Trung, Đà Nẵng
                </li>
                <li>Điện thoại: (0236) 3.888.123</li>
                <li>Liên hệ hợp tác:&nbsp;0835413999</li>
                <li>Email: cloudlearningsystem.cls@gmail.com</li>
              </ul>
            </div>
          </div>
          <div class="col">
            <div>
              <h4>Văn phòng <strong>miền Nam</strong></h4>
              <ul>
                <li>
                  Tầng 8 tòa nhà QTSC 1, Công viên phần mềm Quang Trung P. Tân
                  Chánh Hiệp, Q.12, Hồ Chí Minh
                </li>
                <li>Điện thoại: (028) 3.715.4426</li>
                <li>Liên hệ hợp tác: 0835413999</li>
                <li>Email: cloudlearningsystem.cls@gmail.com</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <hr style="background-color: white; margin: 0" />
      <div class="d-flex justify-content-between align-items-center">
        <div class="p-3">
          <img
            src="https://cls.vn/images/configs/2021/07/14/logo-cls-072021-01-451.png"
            alt="CLS E-Learning"
            width="55px"
          />
          <span style="font-size: 13px; padding: 0 25px">Một sản phẩm của</span>
          <img
            src="https://cls.vn/Content/images/logo-huong-viet-group.png"
            alt="Hương Việt Group"
            width="160px"
          />
        </div>
        <div>
          <img
            src="https://cls.vn/Content/images/xac-nhan-bo-cong-thuong.png"
            alt="bo cong thuong"
            width="130px"
          />
        </div>
        <div>
          <b-icon icon="facebook" class="icon_social"></b-icon>
          <b-icon icon="youtube" class="icon_social"></b-icon>
        </div>
        <div class="payment-icon">
          <img
            src="https://cls.vn/Content/images/logo-icon/pay.png"
            alt="Payment"
          />
        </div>
      </div>
    </b-container>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
h4 {
  font-size: 17px;
  margin-bottom: 25px;
}
strong {
  color: var(--hover-color);
}
ul {
  font-size: 12px;
  margin-left: -25px;
}
li {
  margin: 10px 0;
}
.footer {
  padding: 50px 0 0;
  background-color: var(--main-color);
  color: var(--white-color);
}
.img_QR {
  width: 60px;
  height: 60px;
  margin-left: 5px;
}
.icon_social {
  width: 25px;
  height: 25px;
  margin: 0 5px;
  padding: 5px;
  border: 1px solid #fff;
}
</style>
