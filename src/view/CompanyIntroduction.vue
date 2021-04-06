<template>
    <div id="CompanyIntroduction" >
        <div class="banner container-fuild text-center">
          <img src="../assets/img/banner1.png">
        </div>
      <div class="imgBlock">
        <img src="../assets/img/company.png">
      </div>
        <div class="container">
            <div class="row CompanyIntroduction-container dis-block">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <p class="com-title">合肥中科融道智能科技有限公司</p>
<!--                    <p class=".text-justify">合肥中科融道智能科技有限公司成立于2021年1月。以中科院合肥技术创新工程院为依托，将人工智能核心技术与产业融合，通过提供产品和系统解决方案来推动产业的智能升级转型。</p>-->
                    <p  class="com-title-dis">合肥中科融道智能科技有限公司成立于2021年1月。以中科院合肥技术创新工程院为依托，将人工智能核心技术与产业融合，通过提供产品和系统解决方案来推动产业的智能升级转型。</p>
                </div>
            </div>
        </div>
      <div class="imgBlock">
        <img src="../assets/img/enterprise.png">
      </div>
      <div class="botBlock">
        <img src="../assets/img/idea.png">
      </div>
      <div class="bottom-color"></div>
    </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
    name: 'CompanyIntroduction',
    data(){
        return{

        }
    },
    mounted(){
        var wow = new WOW();
        wow.init();
    }
}
</script>
<style scoped>
.banner{
    color: #fff;
    font-size: 30px;
    line-height: 150px;
    width:100%;
}
.banner img{
  width: 100%;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    /*padding: 100px 0;*/
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
  font-size: 24px;
  line-height: 48px;
}
/*-------------*/
.dis-block{
  background: #ffffff;
  height: 370px;
  color: #5A5858;

}
.bottom-color{
  width: 100%;
  height:15px;
  /*background-color:#ababab26;*/
}
.imgBlock{
  width:100%;
  margin: 160px 0;
}
.botBlock{
  width:100%;
  margin-bottom: 30px ;

}
.botBlock img{
  width:100%;
}
.imgBlock img{
  width: 100%;
}
.com-title{
  font-size: 30px!important;
  font-weight: 600;
  margin: 35px 0;
}
.com-title-dis{
  font-size: 24px;
  /*font-weight: 600;*/
  line-height: 48px;
  text-indent: 3.5rem;
}
/*手机*/
@media screen and (max-width: 768px){
  .imgBlock{
    margin: 60px 0;
  }
}


@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}

}
</style>

