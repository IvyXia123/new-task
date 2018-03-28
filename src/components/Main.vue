<template>
  <div id="mainPage">
    <!--头部导航-->
    <div class="header">
      <div class="nameWrapper">
        <img class="comLogo" src="./../assets/logo.png"/>
        <span class="comName">{{companyName}}</span>
      </div>
      <div class="headerNavWrapper">
        <router-link class="dataManage" tag="a" :to="{name:'dataManagement'}">
          报送数据管理
          <span class="line"></span>
        </router-link>
        <router-link class="servicePaltform" tag="a" :to="{name:'servicePlatform'}">一站式服务平台</router-link>
        <input class="searchBox" type="text" placeholder="请输入关键字"/>
      </div>
      <div class="basicInfoWrapper">
        <span class="time">2018-03-28 星期四 09:45:27</span>
        <img class="moreIcon" src="./../assets/home_preferences.png"/>
        <span class="moreChoice">首选项</span>

      </div>
    </div>
    <!--导航-->
    <div class="navText">
      <span>首页 &gt;</span>
      <span>一站式服务平台 &gt;</span>
      <span>用户管理</span>
    </div>
    <div class="content">
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
  export default {
    name: "mainPage",
    data() {
      return {
        companyName: '上海天正智能数据服务有限公司'
      }
    },
    mounted() {

      layui.use('laydate', function () {
        console.log(layui)
        var laydate = layui.laydate;

//        执行一个laydate实例
        laydate.render({
          elem: '#test1' //指定元素
        });
      });
    }
  }
</script>

<style lang="less" scoped>
  @import "./../less/common";

  #mainPage {
    .w(100%);
    .h(100%);
    .header {
      position: relative;
      .w(100%);
      min-width:1240px;
      .h(60px);
      .p(10px 40px 10px 20px);
      overflow: hidden;
      box-sizing: border-box;
      background: @headerBgColor;
      .nameWrapper {
        .w(300px);
        .h(100%);
        float: left;
        .comLogo {
          .w(40px);
          .h(40px);
          margin-right: 5px;
          vertical-align: middle;
        }
        .comName {
          .f-s(16px);
          color: @whiteColor;
        }
      }
      .headerNavWrapper {
        position: absolute;
        .w(calc(~"100% - 660px"));
        .h(60px);
        .p(10px 6%);
        top: 0;
        left: 320px;
        box-sizing: border-box;
        overflow: hidden;
        .dataManage, .servicePaltform {
          position: relative;
          .h(30px);
          .l-h(30px);
          .f-s(14px);
          margin-top: 3px;
          color: #fefefe;
          margin-right: 25px;
          .d-i(inline-block);
          .line {
            position: absolute;
            .d-i(inline-block);
            .w(50%);
            .h(2px);
            left: 25%;
            bottom: -2px;
            border-bottom: 2px solid #fff;
          }
        }
        .searchBox {
          float: right;
          .h(30px);
          .p(3px 10px);
          .l-h(24px);
          margin-top: 5px;
          box-sizing: border-box;
          outline: none;
          color: @whiteColor;
          border-radius: 15px;
          border: 1px solid @inputBorder;
          .b(@inputBg);
          &::-webkit-input-placeholder {
            color: @whiteColor;
          }
        }
      }
      .basicInfoWrapper {
        .w(300px);
        .h(100%);
        text-align: right;
        float: right;
        color: @whiteColor;
        .time, .moreChoice {
          .d-i(inline-block);
          .h(100%);
          .l-h(40px);
          .f-s(14px);
        }
        .time {
          margin-right: 15px;
        }
        .moreIcon {
          .w(15px);
          .h(13px);
          vertical-align: middle;
        }
        .moreChoice {
        }

        .layui-nav {
          .d-i(inline-block);
        }
      }
    }
    .navText {
      .h(40px);
      .p(5px 20px);
      .b(@bodyBg);
      .l-h(30px);
      .f-s(14px);
      box-sizing: border-box;
    }
    .content {
      .w(100%);
      .h(calc(~"100% - 100px"));
      .p(0 20px 20px);
      /*.b(@bodyBg);*/
      .b(lightblue);
      box-sizing: border-box;
    }


    @media only screen and (min-width: 1400px) {
      .header {
        .headerNavWrapper {
          .p(10px 12%);
        }
      }
    }
  }
</style>
