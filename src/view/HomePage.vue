<template>
  <div id="HomePage">
    <!-- 轮播图 -->
    <div id="swiper" class="container-fuild">
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
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination"></div>

        <!-- 如果需要导航按钮 -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>
    </div>
    <div id="fontShow">
      <div id="blueLine"></div>
      <h1>致力于打造高科技民营企业</h1>
      <h3>COMMITTED TO BUILDING HEIGHT-TECH PRIVATE ENTERPRISES</h3>
    </div>
<!--    框框-->
    <div id="lineBlock">
      <div class="col-xs-3 col-sm-3 col-md-3">
        <div class="bigFont">科技创新</div>
        <div class="smallFont">TECHNOLOGICAL INNOVATION</div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3">
        <div class="bigFont">智慧未来</div>
        <div class="smallFont">SAMRT FUTURE</div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3">
        <div class="bigFont">追求卓越</div>

        <div class="smallFont">PURSUIT OF EXCELLENCE</div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3">
        <div class="bigFont">团队进取</div>
        <div class="smallFont">TEAM SPIRIT</div>
      </div>
    </div>
<!--    产品展示-->
<!--动态-->
    <!--<div id="productBlock" >

      <div class="proLog">
        <img src="../assets/img/proLog.png">
        <div class="proName">
          <p style="font-size: 25px;letter-spacing: 3px">产品介绍</p>
          <p style="margin-top: 18px;font-size: 12px;letter-spacing: 1px">INTRODUCTION</p>
        </div>


      </div>

      <div ></div>
      <div id="customer2" class="container-fuild">
        <div class="container customer-container">
          <div class="swiper-container proSamll hidden-xs">
            <div class="swiper-wrapper">
              <div
                class="swiper-slide customer-block"
                v-for="(item,index) in productList"
                :key="index"
              >
                <div class="customer-logo">
                  <img class="center-block" :src="item.img" >
                </div>

                <div class="customer-content1">
                  <div>{{item.title}}</div>
                </div>
&lt;!&ndash;                <div class="customer-content2">{{item.title}}</div>&ndash;&gt;
              </div>
            </div>
            &lt;!&ndash;&lt;!&ndash; 如果需要分页器 &ndash;&gt;
            <div class="swiper-pagination"></div>
            &lt;!&ndash; 如果需要导航按钮 &ndash;&gt;
            <div class="swiper-button-prev"></div>
            <div class="swiper-button-next"></div>&ndash;&gt;
          </div>
          <div class="row visible-xs customer-block">
            <div class="col-xs-12" v-for="(item,index) in customerList" :key="index">
              <div class="customer-logo">
                <img class="center-block" :src="item.logo" alt="logo">
              </div>
              <div class="customer-yh">
                <img src="@/assets/img/yinhao.png" alt="引号">
              </div>
              <div class="customer-content1">
                <small>{{item.content}}</small>
              </div>
              <div class="customer-content2">
                <small>{{item.title}}</small>
              </div>
            </div>
          </div>

        </div>
      </div>
    </div>-->

    <div id="productBlock" >
      <div class="proLog">
        <img src="../assets/img/proLog.png">
        <div class="proName">
          <p style="font-size: 25px;letter-spacing: 3px">产品介绍</p>
          <p style="margin-top: 18px;font-size: 12px;letter-spacing: 1px">INTRODUCTION</p>
        </div>


      </div>

      <div class="products">
        <div class="product-ph col-xs-12 col-sm-4 col-md-4">
          <div class="customer-logo">
            <img class="center-block" src="../assets/img/pro.png" >
          </div>

          <div class="customer-content1" style="width: 400px;margin: 0 auto;">
            <div class="customer-content-jt">产品描述产品描述产品描述产产品描述产品描述产品描述产产品描述产品描述产品描述产产品描述产品描述产品描述产产品描述产品描述产品描述产产品描述产品描述产品描述产产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述产品描述</div>
          </div>
        </div>
        <div class="product-ph col-xs-12 col-sm-4 col-md-4">
          <div class="customer-logo">
            <img class="center-block" src="../assets/img/pro1.png" >
          </div>

          <div class="customer-content1" style="width: 400px;margin: 0 auto;">
            <div class="customer-content-jt">产品描述</div>
          </div>
        </div>
        <div class="product-ph col-xs-12 col-sm-4 col-md-4">
          <div class="customer-logo">
            <img class="center-block" src="../assets/img/pro2.png" >
          </div>

          <div class="customer-content1" style="width: 400px;margin: 0 auto;">
            <div class="customer-content-jt">产品描述</div>
          </div>
        </div>
      </div>
    </div>



    <div id="contactUs" class="container-fuild text-center">
      <div class="container contactUs-container wow slideInUp">
        <h1>您身边的IT专家</h1>
        <h3>7x24小时提供出色的IT服务</h3>
        <button
          class="btn btn-default btn-sm"
          onmouseleave="this.style.borderColor='#ffffff'; this.style.backgroundColor='#ffffff'; this.style.color='#3f3f3f';"
          onmouseenter="this.style.backgroundColor='transparent'; this.style.borderColor='#ffffff'; this.style.color='#ffffff';"
        >联系我们</button>
        <!--<div class="contactUs-contactWay">
          <span></span>
          <span></span>
          <span></span>
        </div>-->
      </div>
    </div>
    <!--&lt;!&ndash; 客户评价 &ndash;&gt;
    <div id="customer" class="container-fuild">
      <div class="container customer-container">
        <p class="customer-title text-center">客户评价</p>
        <div class="swiper-container customer-swiper hidden-xs">
          <div class="swiper-wrapper">
            <div
              class="swiper-slide customer-block"
              v-for="(item,index) in customerList"
              :key="index"
            >
              <div class="customer-logo">
                <img class="center-block" :src="item.logo" alt="logo">
              </div>
              <div class="customer-yh">
                <img src="@/assets/img/yinhao.png" alt="引号">
              </div>
              <div class="customer-content1">
                <small>{{item.content}}</small>
              </div>
              <div class="customer-content2">{{item.title}}</div>
            </div>
          </div>
          &lt;!&ndash; 如果需要导航按钮 &ndash;&gt;
          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>
        </div>
        <div class="row visible-xs customer-block">
          <div class="col-xs-12" v-for="(item,index) in customerList" :key="index">
            <div class="customer-logo">
              <img class="center-block" :src="item.logo" alt="logo">
            </div>
            <div class="customer-yh">
              <img src="@/assets/img/yinhao.png" alt="引号">
            </div>
            <div class="customer-content1">
              <small>{{item.content}}</small>
            </div>
            <div class="customer-content2">
              <small>{{item.title}}</small>
            </div>
          </div>
        </div>
      </div>
    </div>
    &lt;!&ndash; 为什么选择我们 &ndash;&gt;
    <div id="whyChooseUs" class="conatiner-fuild">
      <div class="container">
        <div class="whyChooseUs-title text-center">
          <p>为什么选择我们的服务</p>
          <p>THE REASON TO CHOOSING US</p>
        </div>
        <div class="row">
          <div
            class="col-xs-12 col-sm-6 col-md-3 server-wrapper"
            v-for="(item,index) in serverList"
            :key="index"
          >
            <div
              class="server-block wow slideInUp"
              onmouseenter="this.style.color='#28f';this.style.borderColor='#28f'"
              onmouseleave="this.style.color='#666';this.style.borderColor='#ccc'"
            >
              <img class="center-block" :src="item.logo" alt="logo">
              <p class="text-center">{{item.title}}</p>
              <div
                class="text-center"
                v-html="item.content"
                onmouseenter="this.style.color='#28f'"
                onmouseleave="this.style.color='#ccc'"
              ></div>
            </div>
          </div>
        </div>
      </div>
    </div>-->
  </div>
</template>
<script>
import Swiper from "swiper";
import { WOW } from 'wowjs';
export default {
  name: "HomePage",
  data() {
    return {
      swiperList: [
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
      ],
      // 产品展示   产品描述改title 一一对应 目前是3页，每页3个
      /*productList:[
        {
          img: require("@/assets/img/pro.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro1.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro2.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro1.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro2.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro1.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
        {
          img: require("@/assets/img/pro2.png"),
          path: "",
          title: "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content: '',
        },
      ],*/
      customerList: [
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_toyota.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_kk.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        },
        {
          logo: require("@/assets/img/logo_hp.png"),
          title:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。",
          content:
            "您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。您可以双击这里或者点击编辑按钮来修改内容。您还可以添加图标，按钮，图片等常用元素。"
        }
      ],
      serverList: [
        {
          logo: require("@/assets/img/tel.png"),
          title: "核心优势1",
          content: "<p>由专业客服提供人工服务</p>负责疑难问题和故障受理"
        },
        {
          logo: require("@/assets/img/computer.png"),
          title: "核心优势2",
          content: "<p>利用远程视频工具，提供协助</p>帮助客户进行调试、解决故障"
        },
        {
          logo: require("@/assets/img/qq.png"),
          title: "核心优势3",
          content: "<p>利用企业QQ提供在线解答</p>帮助企业快速准确解决问题和故障"
        },
        {
          logo: require("@/assets/img/skill.png"),
          title: "核心优势4",
          content: "<p>由技术支持工程师，负责问题解答</p>需求受理及故障受理"
        }
      ]
    };
  },
  mounted() {
    /* banner-swiper */
    new Swiper(".banner-swiper", {
      loop: true, // 循环模式选项
      effect: 'fade',
      speed:2000,
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination",
        clickable: true
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
    });

/*// 产品展示
    var swiper = new Swiper('.proSamll',
      {
        loop: true, // 循环模式选项
        slidesPerView: 3,
        // slidesPerGroup: 3,
        spaceBetween: 110,
        //自动播放
        autoplay: {
          delay: 6000,
          stopOnLastSlide: false,
          disableOnInteraction: false
        },
       /!* // 如果需要分页器
        pagination: {
          el: ".swiper-pagination",
          clickable: true,

        },*!/
        // 如果需要前进后退按钮
        /!*navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        },*!/
        observer: true, //修改swiper自己或子元素时，自动初始化swiper
        observeParents: true //修改swiper的父元素时，自动初始化swiper
      });*/
    /* customer-swiper */
    new Swiper(".customer-swiper", {
      loop: true, // 循环模式选项
      slidesPerView: 3,
      slidesPerGroup: 3,
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
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
  color: #fff;
  height: 400px;
  background: url("../assets/img/contact_us_bg.jpg") 0 0 no-repeat;
  background-size: 100% 100%;
  transition: all ease 0.6s;
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

