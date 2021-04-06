<template>
  <div id="footer" class="container-fluid">
  <!--  <div class="logo">
      <img src="@/assets/img/logo_white.png" alt="logo图">
    </div>
&lt;!&ndash;    <p class="title">公司企业网站模板</p>&ndash;&gt;
    <p class="address_tel_fax">
      <span>地址：合肥市创新大道与明珠大道交口明珠产业园2栋D区3楼</span>
&lt;!&ndash;      <span>Tel：888-888-888</span>&ndash;&gt;
&lt;!&ndash;      <span>Fax：8888-88888888</span>&ndash;&gt;
    </p>
    <p class="email_wx">
      <span>合作邮箱：hw_1988@qq.com</span>
      <span>微信公众号：rongdaoai</span>
    </p>
    <p class="copy">合肥中科融道智能科技有限公司 &copy; 2021 All Rights Reserved. </p>-->
<!--    底部代码-->
    <div class="top-logo">

    </div>
    <div class="midd-mes">
<!--      关于我们-->

      <div class="midd-us col-xs-12 col-sm-4 col-md-4">
        <h2>关于我们</h2>
        <p>公司介绍</p>
        <p>招贤纳士</p>
        <p>公司地址：安徽省合肥市高新区习友路2666号中科院合肥技术创新工程院1号楼416-C</p>
      </div>
      <!--      联系我们-->

      <div class="midd-us col-xs-12 col-sm-4 col-md-4">
        <h2>联系我们</h2>
        <p>合作邮箱：rongdaoai@qq.com</p>
        <img style="cursor: pointer" src="../assets/img/ewm.jpg" @mousemove="showQR()" @mouseout="showDis()">
<!--        <p>商务合作：181XXXXXXXX</p>-->
<!--        <p>媒体合作：180XXXXXXXX</p>-->
<!--        <p>供应商合作：180XXXXXXXX</p>-->
      </div>
      <!--     热线电话-->

      <div class="midd-us col-xs-12 col-sm-4 col-md-4">
  <!--        <h2>全国热线电话</h2>-->
  <!--        <h3>400-8510580 / 0551-65708117 </h3>-->
  <!--        <p>周一到周日09:00-17:30</p>-->
      </div>
    </div>
    <div class="bot-mes">合肥中科融道智能技术有限公司 © 2021 All Rights Reserved. 网站备案号：皖ICP备2021003654号</div>

    <div class="shadow"></div>

  </div>

</template>
<script>
export default {
  name: "Footer",
  data() {
    return {};
  },
  methods:{
    showQR(){
      console.log("ssssssss")
    },
    showDis(){
      console.log("seeeeeeeeeeeeeee")
    }
  }
};
</script>
<style scoped>
#footer {
  margin-top: 20px;
  width: 100%;
  /*height: 482px;*/
  color: #fff;
  /*background: #2d2d2d54;*/
  overflow: hidden;
  text-align: center;
  background-image: url("../assets/img/botBlack.png");
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

/*-----------*/
/*底部样式代码*/
.top-logo{
  width: 100%;
  position: relative;
  height:80px;
  border-bottom: 1px solid #464646;
  margin-bottom: 30px;
}
.midd-mes{
  width:100%;
  height:300px;
  /*display: flex;*/
  /*padding: 30px 0 ;*/
  /*border:1px solid #0ce9f1;*/
  position: relative;
}
.midd-us{
  position: relative;
  /*width:350px;*/
  height:100%;
  /*border: 1px solid #761c19;*/
  top:1%;
  text-align: left;
  line-height: 46px;
  padding: 0 8%;
}
.midd-us h3{
  margin-bottom: 15px;
}
.midd-about{
  left:9%;
}
.midd-cont{
  left:40%;

}
.midd-call{
  right:8%;
}
.midd-us img{
  position: absolute;
  bottom: 15%;
  left:24%;
  width: 120px;
}
.bot-mes{
  width:100%;
  text-align: center;
  line-height: 46px;
  height:40px;
  margin-top: 30px;
  border-top: 1px solid #464646;
}
@media screen and (max-width: 768px){
  .midd-us img{
    left:9%;
  }
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
/*-------------*/







}
</style>

