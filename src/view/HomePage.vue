<template>
  <div id="HomePage">
    <!-- 轮播图 -->
    <!--<div id="swiper" class="container-fuild">
      <div class="swiper-container banner-swiper">
        <div class="swiper-wrapper">
          <div class="swiper-slide" v-for="(item,index) in swiperList" :key="index">
            <img class="swiper-lazy" :data-src="item.img" alt="轮播图">
            <div class="swiper-lazy-preloader"></div>
            <div class="swiper-slide-title">
                <h1>{{item.title}}</h1>
                <p>{{item.content}}</p>
            </div>
          </div>
        </div>
        &lt;!&ndash; 如果需要分页器 &ndash;&gt;
        <div class="swiper-pagination"></div>

        &lt;!&ndash; 如果需要导航按钮 &ndash;&gt;
&lt;!&ndash;        <div class="swiper-button-prev"></div>&ndash;&gt;
&lt;!&ndash;        <div class="swiper-button-next"></div>&ndash;&gt;
      </div>
    </div>-->

<!--    首页大图-->
    <div class="top-img">
      <img src="../assets/img/topImg.png">
    </div>

    <!--    产品介绍-->
    <div class="contact-us">
      <img src="../assets/img/introduction.png">
    </div>

<!--    产品介绍 详细-->
    <div class="introduce-pro">
<!--      <img class="introduce-pro-img" src="../assets/img/intPro.png">-->
      <div class="products-list">
        <div @click="clickPro(0)" class="products-list-block blue-back col-xs-6 col-md-3">
          <img  class="pro1" src="../assets/img/pro1.png">
          <p>智能网络摄像机</p>
        </div>
        <div @click="clickPro(1)" class="products-list-block col-xs-6 col-md-3">
          <img class="pro2" src="../assets/img/pro2.png">
          <p>智能物联网主机</p>
        </div>
        <div @click="clickPro(2)" class="products-list-block col-xs-6 col-md-3">
          <img class="pro3" src="../assets/img/pro3.png">
          <p>电力解决方案</p>
        </div>
        <div @click="clickPro(3)" class="products-list-block col-xs-6 col-md-3">
          <img class="pro4"src="../assets/img/pro4.png">
          <p>智能园区</p>
        </div>
      </div>
      <div class="products-list-mes">
        <div class="dis-pro">
          <p class="title-pro">{{ showName }}</p>
          <p>{{ showMes }} ...</p>
        <div class="more-pro"></div>
        </div>
        <div class="img-pro">
        </div>
       </div>
    </div>

<!--    联系我们-->
    <div class="contact-us">
      <img src="../assets/img/callUs.png">
    </div>

<!--    融合智能科技 . 建设美好生活-->
    <div id="contactUs" class="container-fuild text-center">
      <img src="../assets/img/rhzn.png">
    </div>




  </div>
</template>
<script>
import Swiper from "swiper";
import { WOW } from 'wowjs';
export default {
  name: "HomePage",
  data() {
    return {
      /*swiperList: [
        {
          img: require("@/assets/img/newBanner.png"),
          path: "",
          title: '',
          content: '',
        },
        // {
        //   img: require("@/assets/img/banner2.jpg"),
        //   path: "",
        //   title: '',
        //   content: '',
        // },
        // {
        //   img: require("@/assets/img/banner1.png"),
        //   path: "",
        //   title: '',
        //   content: '',
        // },
        {
          img: require("@/assets/img/newBanner1.png"),
          path: "",
          title: '',
          content: '',
        }
      ],*/

      showName:'智能网络摄像机',
      showMes:'系列智能网络摄像机内嵌深度学习算法，可提供精准的人脸侦测、人车分类侦测、越界侦测、区域入侵侦测、轨迹跟踪、进入/离开区域侦测等功能。能够进行行为分析、智能报警、联动报警。支持3D数字降噪、强光抑制、背光补偿、电子防抖等，使得图像和音频具有较好的质量。在超高分辨率下可输出实时图像',

      names:['智能网络摄像机','智能物联网主机','电力解决方案','智能园区'],
      mes:['系列智能网络摄像机内嵌深度学习算法，可提供精准的人脸侦测、人车分类侦测、越界侦测、区域入侵侦测、轨迹跟踪、进入/离开区域侦测等功能。能够进行行为分析、智能报警、联动报警。支持3D数字降噪、强光抑制、背光补偿、电子防抖等，使得图像和音频具有较好的质量。在超高分辨率下可输出实时图像',
            '智能物联网主机高度集成化模块化智能数据采集产品，具备视频采集、视频智能分析、视频存储、物联数据采集、单向安全传输、数据过滤、数据加密、数据分析预警等丰富功能。主机可海量接入企业自动化控制系统、安全仪表系统等控制系统的安全参数和报警数据，包括液位、温度、压力、气体浓度等安全参数',
            '基于融道自研的融+算法平台，通过多层次体系构建，深度赋能电力行业输变配等各个方向。在输电领域，汇聚融合输电专业相关业务系统数据，实现设备运行、通道环境、作业现场、灾害预警等输电全业务全景数据可视化展示及智能联动决策分析，支撑输电运检人员对设备和通道运行状况进行监测和跟踪，精确掌握设备实时状态',
            '运用物联网、车联网、AI、大数据、移动互联等现代技术，开发智慧园区解决方案，助力各类园区构建统一的信息化基础架构体系，搭建园区统一接入标准，构建智慧化的园区系统，从而为提升园区管理者的服务水平，提高工作效率提供强力支撑。系统全面集成各类设备、传感器，依托智慧园区平台强大的通讯能力'],


    };
  },
  methods:{
    clickPro(index){
      console.log("index: ",index)
      var aa = $('.products-list-block')[index];
      var bb = $('.img-pro')[0];
      $(aa).addClass("blue-back").siblings('div').removeClass("blue-back");
      $(bb).addClass("img-pro"+index);

      var nums = [0,1,2,3];
      var unmIndex = index;

      $.each(nums,function (index,val){
        if(val == unmIndex){
          console.log(val)
        }else{
          $(bb).removeClass("img-pro"+val);
        }
      })
      this.showName = this.names[index];
      this.showMes = this.mes[index];
    }
  },
  mounted() {
    /* banner-swiper */
/*    new Swiper(".banner-swiper", {
      loop: true, // 循环模式选项
      effect: 'fade',
      speed:2000,
      // pagination:'custom',
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination",
        clickable: true,
        type:'fraction'
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      // 延迟加载
      lazy: {
        loadPrevNext: true
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });*/

    /* wowjs动画 */
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    })
    wow.init();
  }
};
</script>
<style scoped>
/* 整体盒子 */
#HomePage {
  width: 100%;
  /*background-color: #ababab26;*/
}

/* 轮播图 */
#swiper {
  height: 600px;
}
#swiper .banner-swiper {
  width: 100%;
  height: 100%;
}
#swiper .banner-swiper .swiper-slide img {
  width: 100%;
  height: 100%;
}
#swiper .banner-swiper .swiper-slide{
  position: relative;
}
#swiper .banner-swiper .swiper-slide-title {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 999999999;
  width: 100%;
  height: 100%;
  color: #fff;
  /*background: rgba(51, 51, 51, 0.534);*/
  text-align: center;
  line-height: 80px;
}
#swiper .banner-swiper .swiper-slide-title > h1{
  font-size: 50px;
  margin-top: 12%;
}
#swiper .banner-swiper .swiper-slide-title > p{
  font-size: 20px;
  margin-top: 1%;
  font-weight: 700;
}
/* 大数据管理系统 */
#bigData {
  padding: 100px;
  transition: all ease 0.6s;
  box-sizing: border-box;
}
#bigData .bigData-title {
  padding-bottom: 10px;
  border-bottom: 1px solid #ccc;
}
#bigData p {
  font-size: 14px;
  color: #333;
  line-height: 2rem;
}
#bigData .bigData-device {
  margin: 50px 0 20px;
}

/* 您身边的IT专家 */
#contactUs {
  width:100%;
  /*height: 500px;*/
  /*background: url("../assets/img/contact_us_bg.jpg") 0 0 no-repeat;*/
  /*background: url("../assets/img/rhzn.png") 0 0 no-repeat;
  background-size: 100% 100%;
  transition: all ease 0.6s;*/
}
#contactUs img{
  width:100%;
}
#contactUs .contactUs-container {
  padding-top: 50px;
}
#contactUs .contactUs-container button {
  width: 300px;
  height: 50px;
  margin-top: 40px;
}
#contactUs .contactUs-container .contactUs-contactWay span {
  display: inline-block;
  width: 48px;
  height: 48px;
  margin: 30px;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(1) {
  background: url("../assets/img/weixin.png") 0 0 no-repeat;
  background-size: 100% 100%;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(2) {
  background: url("../assets/img/weibo.png") 0 0 no-repeat;
  background-size: 100% 100%;
}
#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(3) {
  background: url("../assets/img/twitter.png") 0 0 no-repeat;
  background-size: 100% 100%;
}

/* 客户评价 */
#customer {
  padding: 50px 0;
  box-sizing: border-box;
  background: #efefef;
  transition: all ease 0.6s;
}
#customer .customer-title {
  font-size: 30px;
  color: rgb(102, 102, 102);
  margin: 0 0 30px;
}
#customer .customer-block {
  background: #fff;
  padding: 30px;
}
#customer .customer-logo img {
  width: 94px;
  height: 94px;
  border: 1px solid #ccc;
}
#customer .customer-yh img {
  width: 34px;
  height: 34px;
}
#customer .customer-content1 {
  padding-bottom: 20px;
  border-bottom: 1px solid #0ce9f1;
}
#customer .customer-content2 {
  padding-top: 20px;
}
/* 为什么选择我们 */
#whyChooseUs {
  padding: 100px;
}
#whyChooseUs .whyChooseUs-title {
  margin-bottom: 50px;
}
#whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
  font-size: 25px;
  font-weight: 500;
}
#whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
  font-size: 14px;
}
#whyChooseUs .server-block {
  padding: 50px 20px;
  border: 1px solid #ccc;
  border-bottom: 5px solid #ccc;
}
#whyChooseUs .server-block img {
  width: 48px;
  height: 48px;
}
#whyChooseUs .server-block > p {
  font-size: 20px;
  margin: 30px 0;
}
#whyChooseUs .server-block > div {
  color: #ccc;
}

/*-----------------------------*/
/*添加模块*/

.top-img{
  width:100%;
}
.top-img img{
  width:100%;
}
#fontShow{
  height:140px;
  padding:1%;
  width:100%;
  text-align: center;
  /*padding-top:2%*/
  /*width: 100%;*/
}
#blueLine{
  width: 80px;
  height: 6px;
  background-color: #1e73be;
  border-radius: 5px;
  margin: 5px auto;
}
#fontShow h1{
  /*margin: 10px auto;
  width: 435px;*/
}
#fontShow h3{
  /*margin: 10px auto;
  width: 760px;*/
}

#lineBlock{
  height: 152px;
  margin: 10px auto;
  width: 1160px;
  border: 1px solid #000000;
  display: flex;
  text-align: center;
}

.smallBlock{
  margin: 9px 0;
  padding: 22px;
  /*border: 1px dashed salmon;*/
  text-align: center;
  color: black;


}
.bigFont{
  margin: 30px 0;
  font-size: 25px;
  letter-spacing: 5px;
}
.smallFont{
  padding:0;
  font-size:15px;
  letter-spacing: 1px;
}

/*静态产品*/
.customer-content-jt {
  /*margin: 20px 0;*/
  /*padding-bottom: 20px;*/
  line-height: 27px;
  font-size: 16px;
  height:190px;
  padding: 8px;
  background-color: #9392925c;
  text-indent:2em;
  overflow-y: auto;
  border-radius: 0 0 10px 10px;
  /*border-bottom: 1px solid #0ce9f1;*/
}
/*联系我们*/
.contact-us{
  width:100%;
  /*height:104px;*/
  /*background: #761c19;*/
  /*background: url("../assets/img/callUs.png") 0 0 no-repeat;*/
  /*display: flex;*/
  /*position: relative;*/
  margin: 150px 0;
}
.contact-us img{
  width: 100%;
}
/*产品*/
.introduce-pro{
  width:100%;
  /*height:910px;*/
  margin-top: 30px;
  /*position: relative;*/
  /*display: flex;*/
  background-image: url("../assets/img/intPro.png");
  background-repeat: no-repeat;
  background-position: 0 0 ;
  background-size: 100%;
  padding:0 15%;
}
.introduce-pro-img{
  position: absolute;
  top:0;
  left:0;
  width:100%;
  z-index: 11;
}
.products-list{
  width:100%;
  height:450px;
  background: #7698bb00;
}

.products-list img{
  margin: 150px auto;
}
.products-list-block{
  height: 100%;
  border: 1px solid #ffffff36;
  position: relative;
  cursor: pointer;
}
.blue-back{
  background-image: url("../assets/img/blueBack.png");
}
.products-list-block p{
  width: 92%;
  text-align: center;
  color: #ffffff;
  position: absolute;
  font-size: 24px;
  bottom:8%;

}

.pro1{
  width:230px;
}
.pro2{
  width:216px;
  margin-top: 190px!important;
}
.pro3{
  width:257px;
  margin-top: 165px!important;
}
.pro4{
  width:247px;
  margin-top: 128px!important;
}
.products-list-mes{
  width:100%;
  background: #ffffff;
  height: 450px;
  /*border: 1px solid #0ce9f1;*/
  padding:75px 50px;
  display: flex;
}
.dis-pro{
  float: left;
  width:75%;
  height:100%;
  font-size: 22px;
  font-weight: 300;
  color: #5A5858;
  line-height: 44px;
  position: relative;

}
.title-pro{
  color: #0646A7;
  font-size: 36px;
  font-weight: 600;
}
.more-pro{
  position: absolute;
  bottom: -30px;
  left:2px;
  margin-top: 30px;
  width:150px;
  height:50px;
  background-image: url("../assets/img/morePro.png");
}
.img-pro{
  margin:62px 30px;
  width:268px;
  height: 164px;
  background: url("../assets/img/pro1.png") no-repeat;
  /*border: 1px solid #0ce9f1;*/
}
.img-pro0{
  background: url("../assets/img/pro1.png") no-repeat;
}
.img-pro1{
  background: url("../assets/img/pro2.png") no-repeat;
}
.img-pro2{
  background: url("../assets/img/pro3.png") no-repeat;
}
.img-pro3{
  background: url("../assets/img/pro4.png") no-repeat;
}

/*融合智能科技*/
.font-mes{
  width: 340px;
  height: 80px;
  line-height: 80px;
  text-align: center;
  margin: 60px auto;
  border: 1px solid #ffffff;
  font-size: 18px;
}

/* 客户评价 */
#productBlock{
  width:80%;
  position: relative;
  /*background-color: #1e73be;*/
  margin: 10px auto;
  padding:10px 30px;
  height:600px;

  /*background-color: aqua;*/
}
.proLog{
  display: flex;
  margin:10px auto;
  width:185px;
  /*margin-top: 10px ;*/
  /*margin-bottom: 10px ;*/
}
.proLog img{
  width: 48px;
  height: 54px;
}
.proName{
  text-align: center;
  line-height: 12px;
  width: 170px;
  padding: 10px;
}
.products{
  width: 100%;
  height:86%;
  /*margin: 10px auto;*/
  /*background-color: #57500e;*/
}
.proSamll{
  height:100%;
  position: relative;

  /*padding:20%;*/
  /*background-color:#761c19 ;*/
}
.samll000{
  background-color: #1b6d85;
  margin: 6% auto;
  width: 95%;
  height: 92%;
}
.logoBlock{
  width:100%;
  height:40%;
  /*background-color: #0ce9f1;*/
}
.disBlock{
  width:100%;
}

#customer2 .customer-logo img {
  width: 400px;
  height: 270px;
  /*border: 1px solid #ccc;*/
}
#customer2 .customer-content1 {
  /*margin: 20px 0;*/
  /*padding-bottom: 20px;*/
  line-height: 27px;
  font-size: 16px;
  height:190px;
  padding: 8px;
  background-color: #9392925c;
  text-indent:2em;
  overflow-y: auto;

  /*border-bottom: 1px solid #0ce9f1;*/
}







/* 媒体查询（手机） */
@media screen and (max-width: 768px) {
  #swiper {
    height: 200px;
  }
  #bigData {
    padding: 30px;
  }
  #bigData .bigData-title {
    font-size: 20px;
  }
  #bigData .bigData-device {
    font-size: 20px;
    margin: 10px 0 10px;
  }
  #contactUs {
    height: 200px;
    transition: all ease 0.6s;
  }
  #contactUs .contactUs-container {
    padding-top: 0;
  }
  #contactUs .contactUs-container h1 {
    font-size: 25px;
  }
  #contactUs .contactUs-container h3 {
    font-size: 18px;
  }
  #contactUs .contactUs-container button {
    width: 200px;
    height: 30px;
    margin-top: 20px;
  }
  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 28px;
    height: 28px;
    margin: 10px;
  }
  #customer {
    padding: 30px 0;
    box-sizing: border-box;
    background: #fff;
  }
  #customer .customer-title {
    font-size: 16px;
    font-weight: bold;
  }
  #customer .customer-logo img {
    width: 48px;
    height: 48px;
  }
  #customer .customer-block {
    padding: 30px;
  }
  #customer .customer-block > div {
    padding: 30px 0;
  }
  #whyChooseUs {
    padding: 20px 0;
    transition: all ease 0.6s;
  }
  #whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
    font-size: 20px;
    font-weight: 700;
  }
  #whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
    font-size: 12px;
  }
  #whyChooseUs .server-block {
    padding: 50px 0;
    border: 1px solid #ccc;
    border-bottom: 5px solid #ccc;
  }
  #whyChooseUs .server-block img {
    width: 48px;
    height: 48px;
  }
  #whyChooseUs .server-block > p {
    font-size: 20px;
    margin: 30px 0;
  }
  #whyChooseUs .server-block > div {
    color: #ccc;
  }
  /*---------------------------------*/
  /*添加模块*/
  #fontShow{
    height:140px;
    padding:1%;
    width:100%;
    text-align: center;
    /*padding-top:2%*/
    /*width: 100%;*/
  }
  #blueLine{
    width: 80px;
    height: 6px;
    background-color: #1e73be;
    border-radius: 5px;
    margin: 5px auto;
  }
  #fontShow h1{
    /*margin: 10px auto;
    width: 435px;*/
    font-size: 34px;
  }
  #fontShow h3{
   /* margin: 10px auto;
    width: 760px;*/
    font-size: 13px;
  }

  #lineBlock{
    height: 128px;
    margin: 10px auto;
    width: 100%;
    border: 1px solid #000000;
    /*display: flex;*/
    text-align: center;
  }

  .bigFont{
    font-size: 14px;
    margin: 20px 0;
  }
  .smallFont{
    font-size: 11px;
  }

  /*静态产品*/
  .customer-content-jt {
    /*margin: 20px 0;*/
    /*padding-bottom: 20px;*/
    line-height: 27px;
    font-size: 16px;
    height:190px;
    padding: 8px;
    background-color: #9392925c;
    text-indent:2em;
    overflow-y: auto;
    border-radius: 0 0 10px 10px;
    /*border-bottom: 1px solid #0ce9f1;*/
  }

  /* 客户评价 */
  #productBlock{
    /*width:80%;*/
    width:100%;
    position: relative;
    /*background-color: #1e73be;*/
    margin: 25px auto;
    padding:0;
    height:1540px;
    /*height:600px;*/
    /*background-color: aqua;*/
  }
  .proLog{
    display: flex;
    margin:10px auto;
    width:185px;
    /*margin-top: 10px ;*/
    /*margin-bottom: 10px ;*/
    width: 210px;
    margin: 10px auto;
  }
  .proLog img{
    width: 48px;
    height: 54px;
  }
  .proName{
    margin-left: 10px;
    text-align: center;
    line-height: 12px;
    /*width: 170px;*/
    padding: 10px;
  }
  .products{
    width: 100%;
    height:480px;
    /*margin: 10px auto;*/
    /*background-color: #57500e;*/
  }
  .product-ph{
    height: 100%;
  }
  .proSamll{
    height:100%;
    position: relative;

    /*padding:20%;*/
    /*background-color:#761c19 ;*/
  }
  .samll000{
    background-color: #1b6d85;
    margin: 6% auto;
    width: 95%;
    height: 92%;
  }
  .logoBlock{
    width:100%;
    height:40%;
    /*background-color: #0ce9f1;*/
  }
  .disBlock{
    width:100%;
  }

  #customer2 .customer-logo img {
    width: 400px;
    height: 270px;
    /*border: 1px solid #ccc;*/
  }
  #customer2 .customer-content1 {
    /*margin: 20px 0;*/
    /*padding-bottom: 20px;*/
    line-height: 27px;
    font-size: 16px;
    height:190px;
    padding: 8px;
    background-color: #9392925c;
    text-indent:2em;
    overflow-y: auto;

    /*border-bottom: 1px solid #0ce9f1;*/
  }
}


/* 媒体查询（平板） */
@media screen and (min-width: 768px) and (max-width: 996px) {
  #swiper {
    height: 400px;
  }
  #bigData {
    padding: 60px;
  }
  #bigData .bigData-title {
    font-size: 30px;
  }
  #bigData .bigData-device {
    font-size: 30px;
    margin: 30px 0 15px;
  }
  #contactUs {
    height: 300px;
  }
  #contactUs .contactUs-container {
    padding-top: 50px;
  }
  #contactUs .contactUs-container h1 {
    font-size: 30px;
  }
  #contactUs .contactUs-container h3 {
    font-size: 20px;
  }
  #contactUs .contactUs-container button {
    width: 300px;
    height: 50px;
    margin-top: 30px;
  }
  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 32px;
    height: 32px;
    margin: 15px;
  }
  #customer .customer-title {
    font-size: 24px;
  }
  #whyChooseUs {
    padding: 20px 0;
  }
  /*----------------------------*/
  /*添加模块*/
  #fontShow{
    height:140px;
    padding:1%;
    width:100%;
    text-align: center;
    /*padding-top:2%*/
    /*width: 100%;*/
  }
  #blueLine{
    width: 80px;
    height: 6px;
    background-color: #1e73be;
    border-radius: 5px;
    margin: 5px auto;
  }
  #fontShow h1{
    /*margin: 10px auto;*/
    /*width: 435px;*/
  }
  #fontShow h3{
    /*margin: 10px auto;*/
    /*width: 760px;*/
  }

  #lineBlock{
    height: 152px;
    margin: 10px auto;
    width: 1160px;
    border: 1px solid #000000;
    display: flex;
    text-align: center;
  }

  .bigFont{
    margin: 30px 0;
    font-size: 25px;
    letter-spacing: 5px;
  }
  .smallFont{
    font-size:15px;
    letter-spacing: 1px;
  }

  /*静态产品*/
  .customer-content-jt {
    /*margin: 20px 0;*/
    /*padding-bottom: 20px;*/
    line-height: 27px;
    font-size: 16px;
    height:190px;
    padding: 8px;
    background-color: #9392925c;
    text-indent:2em;
    overflow-y: auto;
    border-radius: 0 0 10px 10px;
    /*border-bottom: 1px solid #0ce9f1;*/
  }

  /* 客户评价 */
  #productBlock{
    width:80%;
    position: relative;
    /*background-color: #1e73be;*/
    margin: 10px auto;
    padding:10px 30px;
    height:600px;
    /*background-color: aqua;*/
  }
  .proLog{
    margin:10px auto;
    width:185px;
    display: flex;
    margin-top: 10px ;
    margin-bottom: 10px ;
  }
  .proLog img{
    width: 48px;
    height: 54px;
  }
  .proName{
    text-align: center;
    line-height: 12px;
    width: 170px;
    padding: 10px;
  }
  .products{
    width: 100%;
    height:86%;
    /*margin: 10px auto;*/
    /*background-color: #57500e;*/
  }
  .proSamll{
    height:100%;
    position: relative;

    /*padding:20%;*/
    /*background-color:#761c19 ;*/
  }
  .samll000{
    background-color: #1b6d85;
    margin: 6% auto;
    width: 95%;
    height: 92%;
  }
  .logoBlock{
    width:100%;
    height:40%;
    /*background-color: #0ce9f1;*/
  }
  .disBlock{
    width:100%;
  }

  #customer2 .customer-logo img {
    width: 400px;
    height: 270px;
    /*border: 1px solid #ccc;*/
  }
  #customer2 .customer-content1 {
    /*margin: 20px 0;*/
    /*padding-bottom: 20px;*/
    line-height: 27px;
    font-size: 16px;
    height:190px;
    padding: 8px;
    background-color: #9392925c;
    text-indent:2em;
    overflow-y: auto;

    /*border-bottom: 1px solid #0ce9f1;*/
  }
}

</style>

