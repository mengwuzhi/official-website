<template>
  <div id="JobChance">
    <div class="banner container-fuild text-center"></div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-12">
          <div class="JobChance-container wow pulse">
            <h2>Java工程师</h2>
            <p>岗位职责</p>
            <ol>
              <li>负责公司产品及项目系统的功能开发、代码优化；</li>
              <li>及时解决项目中的关键问题和技术难题；</li>
              <li>协助测试人员完成测试。</li>
            </ol>
            <p>任职要求</p>
            <ol>
              <li>本科及以上学历，三年开发经验，计算机或相关专业，有大型网站或B/S架构系统开发工作经验者优先；</li>
              <li>熟练掌握Java语言，具备一年以上web开发经验，能独立解决工作中遇到的问题；</li>
              <li>熟练使用Oracle,SQLServer,MySQL中至少一种数据库系统，并具有基本sql语言编写的能力；</li>
              <li>熟悉常见的数据结构和算法，具备良好的编程习惯及较强的文档编写能力；</li>
              <li>熟悉html、div、css和javascript技术，有一定的前端基础；</li>
              <li>做事严谨踏实，责任心强，条理清楚，善于学习总结，有良好的团队合作精神和沟通协调能力。</li>
            </ol>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from 'wowjs';
export default {
  name: "JobChance",
  data() {
    return {};
  },
  mounted(){
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}
.JobChance-container {
  margin: 100px;
  padding: 30px;
  transition: all ease 0.5s;
  border: 1px dashed salmon;
}
.JobChance-container h2{
  color: rgb(255, 102, 19);
  font-weight: bolder;
  text-align: center;
}
.JobChance-container p{
font-size: 20px;
  color: rgb(255, 102, 19);
  font-weight: 700;
}
.JobChance-container ol{
    list-style-type: decimal;
    padding-left: 30px;
}
.JobChance-container ol>li{
    font-size: 14px;
    line-height: 2.7rem;
}
@media screen and (max-width: 997px) {
  .JobChance-container {
    margin: 20px 0;
    padding: 20px;
    border: 1px dashed salmon;
  }
}
</style>

