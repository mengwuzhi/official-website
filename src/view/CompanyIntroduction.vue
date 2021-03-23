<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center"></div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>合肥中科融道智能科技有限公司</h3>
                    <p class=".text-justify">合肥中科融道智能科技有限公司成立于2021年1月。以中科院合肥技术创新工程院为依托，将人工智能核心技术与产业融合，通过提供产品和系统解决方案来推动产业的智能升级转型。</p>
                    <p class=".text-justify">公司以计算机视觉、语音识别为代表的人工智能技术为基础，聚焦能源行业，形成人工智能在电力特定场景的初步应用，逐步实现软、硬件结合的人工智能综合解决方案，推动公司核心技术、软硬件产品与实体经济深度融合，助力共建共治共享的社会治理新格局。</p>
                </div>
            </div>
        </div>
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
    height: 150px;
    line-height: 150px;
    background-image: url('../assets/img/banner1.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-attachment: scroll;
    background-position: center center;
}
.row{
    margin-right: 0;
    margin-left: 0;
}
.CompanyIntroduction-container{
    padding: 100px 0;
    color: #808080;
    transition: all ease 0.5s;
}
.CompanyIntroduction-container>div>p{
    font-size: 14px;
    line-height: 2.5rem;
}
@media screen and (max-width: 997px){
    .CompanyIntroduction-container{
    padding: 10px 0;
    color: #808080;
}
}
</style>

