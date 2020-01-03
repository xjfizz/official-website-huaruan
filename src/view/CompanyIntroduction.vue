<!--
 * @Author: your name
 * @Date: 2020-01-02 09:15:59
 * @LastEditTime : 2020-01-02 10:41:58
 * @LastEditors  : Please set LastEditors
 * @Description: In User Settings Edit
 * @FilePath: \official-website-master\src\view\CompanyIntroduction.vue
 -->
<template>
    <div id="CompanyIntroduction">
        <div class="banner container-fuild text-center">关于我们</div>
        <div class="container">
            <div class="row CompanyIntroduction-container">
                <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
                    <img class="img-responsive center-block" src="@/assets/img/about_img1.png">
                </div>
                <div class="col-xs-12 col-sm-12 col-md-6">
                    <h3>江苏华软智能信息科技有限公司</h3>
                    <p class=".text-justify">苏州华软智能科技有限公司位于苏州吴江经济开发区五方路，是一家以软件开发为主的高科技民营公司。</p>
                    <p class=".text-justify">公司主要经营网络科技，自成立以来一直从事软件应用开发等相关产业。</p>
                    <p class=".text-justify">苏州华软智能科技有限公司主要经营范围包括：计算机硬件领域内的技术开发、技术咨询、技术转让、技术服务。</p>
                    <p class=".text-justify">销售计算机软硬件一级为外部设备、电子产品、自动化系统、通讯设备。</p>
                     <p class=".text-justify">此外，苏州华软智能科技有限公司现阶段已软件定制为主，推广运营为辅，主要涉及APP开发、微信开发，企业级管理系统开发等。</p>
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

