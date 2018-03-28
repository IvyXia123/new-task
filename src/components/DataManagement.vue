<template>
    <div id="dataManage">
      <div class="leftWrapper">
        <div class="leftContent">
          <div class="topWrapper">

          </div>
          <div class="bottomWrapper">
            <ul class="layui-nav layui-nav-tree"  lay-filter="test">
              <li class="layui-nav-item layui-nav-itemed">
                <a class="" href="javascript:;">所有商品</a>
                <dl class="layui-nav-child">
                  <dd><a href="javascript:;">列表一</a></dd>
                  <dd><a href="javascript:;">列表二</a></dd>
                  <dd><a href="javascript:;">列表三</a></dd>
                  <dd><a href="">超链接</a></dd>
                </dl>
              </li>
              <li class="layui-nav-item">
                <a href="javascript:;">解决方案</a>
                <dl class="layui-nav-child">
                  <dd><a href="javascript:;">列表一</a></dd>
                  <dd><a href="javascript:;">列表二</a></dd>
                  <dd><a href="">超链接</a></dd>
                </dl>
              </li>
              <li class="layui-nav-item"><a href="">云市场</a></li>
              <li class="layui-nav-item"><a href="">发布商品</a></li>
            </ul>
          </div>
        </div>
      </div>
      <div class="rightWrapper">

      </div>
    </div>
</template>

<script>
    export default {
        name: "data-manage"
    }
</script>

<style lang="less" scoped>
  @import "./../less/common";
  #dataManage{
    display:flex;
    .w(100%);
    .h(100%);
    .b(lightyellow);
    .leftWrapper{
      .w(240px);
      .h(100%);
      padding-right:20px;
      box-sizing:border-box;
      .b(lightgreen);
      .leftContent{
        .w(100%);
        .h(100%);
        border-radius:7px;
        box-shadow:1px 1px 1px rgba(0,0,0,0.3);
        .topWrapper{
          .w(100%);
          .h(120px);
          .b(@contentBg);
          border-top-left-radius: 7px;
          border-top-right-radius: 7px;
        }
        .bottomWrapper{
          .w(100%);
          .h(calc(~"100% - 120px"));
          .b(@whiteColor);
          border-bottom-left-radius: 7px;
          border-bottom-right-radius: 7px;
          .layui-nav-tree{
            .w(100%);
          }
          .layui-nav{
            .b(@whiteColor);
            li{
              a{
                color:@blackColor;
              }
            }
          }
        }
      }
    }
    .rightWrapper{
      flex:1;
      background:red;
    }
  }
</style>
