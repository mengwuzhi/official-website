<template>
  <div id="footer" class="container-fluid">
    <div class="logo">
      <img src="@/assets/img/logo_white.png" alt="logo图">
    </div>
<!--    <p class="title">公司企业网站模板</p>-->
    <p class="address_tel_fax">
      <span>地址：合肥市创新大道与明珠大道交口明珠产业园2栋D区3楼</span>
<!--      <span>Tel：888-888-888</span>-->
<!--      <span>Fax：8888-88888888</span>-->
    </p>
    <p class="email_wx">
      <span>合作邮箱：rongdaoai@qq.com</span>
      <span>微信公众号：rongdaoai</span>
    </p>
    <p class="copy">合肥中科融道智能科技有限公司 &copy; 2021 All Rights Reserved. </p>
  </div>
</template>
<script>
export default {
  name: "Footer",
  data() {
    return {};
  }
};
</script>
<style scoped>
#footer {
  width: 100%;
  height: 100%;
  color: #fff;
  background: #474747;
  overflow: hidden;
  text-align: center;
}
.logo {
  width: 95px;
  height: 45px;
  margin: 50px auto 20px;
}
.title {
  font-size: 25px;
  margin-bottom: 20px;
}
.address_tel_fax {
  color: #d3d3d3;
  font-size: 14px;
  margin: 10px 0;
}
.email_wx {
  color: #d3d3d3;
  font-size: 14px;
}
.copy {
  color: #d3d3d3;
  font-size: 14px;
  margin: 50px 0 10px;
}
@media screen and (max-width: 997px) {
  .title {
    font-size: 20px;
  }
  .address_tel_fax {
    font-size: 12px;
  }
  .email_wx {

  font-size: 12px;
}
.copy {
  font-size: 12px;
  margin: 30px 0 10px;
}
}
</style>

