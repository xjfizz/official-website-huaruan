<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">相关服务</div>
    <div class="container">
      <div class="row">
        <div class="col-xs-12 col-sm-12 col-md-3" id="myScrollspy">
          <ul class="nav nav-tabs nav-stacked center-block" id="myNav">
            <p>特色服务</p>
            <li
              :class="item.id==id?'active':''"
              v-for="(item,index) in serviceNavList"
              :key="index"
            >
              <a :href="'#'+item.id">{{item.title}}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div class="content-block" v-for="(item,index) in serviceContentList" :key="index">
            <h2 :id="item.id">
              {{item.title}}
              <small>/ {{item.eng_title}}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import { WOW } from "wowjs";
export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "WEB开发"
        },
        {
          id: "section-2",
          title: "APP开发"
        },
        {
          id: "section-3",
          title: "微信开发"
        },
        {
          id: "section-4",
          title: "人工智能"
        }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "WEB开发",
          eng_title: "APP development",
          content:
            "<h3>主要方向</h3><p>我们的主要研发精力聚焦在服务器开发上，使得我们可以定制任何行业的软件，无论是传统企业的管理软件还是硬件页的工程程序，我们都可以给出全面的解决方案。</p>"
        },
        {
          id: "section-2",
          title: "APP开发",
          eng_title: "APP development",
          content:
            "<h3>主要方向</h3><p>借力于移动开发团队，包括android/ios,涉及领域包括企业级app、商城、物流等，可以使您的系统可覆盖全球95%以上的手机用户，彻底融入用户生活中。</p>"
        },
        {
          id: "section-3",
          title: "微信开发",
          eng_title: "WeChat development",
          content:
            "<h3>主要方向</h3><p>致力于微信小程序和微信公众号开发，包括为微信公众号进行业务开发，为移动应用、PC端网站、公众号第三方平台（为各行各业公众号运营者提供服务）的开发</p>"
        },
        {
          id: "section-4",
          title: "人工智能",
          eng_title: "Artificial intelligence",
          content:
            "<h3>主要方向</h3><p>人工智能是研究使计算机来模拟人的某些思维过程和智能行为（如学习、推理、思考、规划等）的学科，主要包括计算机实现智能的原理、制造类似于人脑智能的计算机，使计算机能实现更高层次的应用。</p>"
        }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
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
ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}
ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}
ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}
ul.nav-tabs li:first-child {
  border-top: none;
}
ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}
ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}
ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}
ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}
ul.nav-tabs.affix {
  top: 30px;
}
.content-block {
  margin: 50px 0;
}
.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
