<template>
    <div id="dataManage">
      <div class="leftWrapper">

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
    }
    .rightWrapper{

      flex:1;
      background:red;
    }
  }
</style>
