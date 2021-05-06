<template>
  <div id="HeaderWrapper">
    <div id="headerTitle">
      <span>{{ massage }}</span>
    </div>
    <div id="headerFunction">
      
      <router-link to="/login">
        <el-button class="btn">系统登陆</el-button>
      </router-link>
      <router-link to="/register">
        <el-button class="btn">注册界面</el-button>
      </router-link>
      <router-link to="/work">
        <el-button class="btn">工作中心</el-button>
      </router-link>
      <router-link to="/reader">
        <el-button class="btn">读者信息</el-button>
      </router-link>
      <router-link to="/book">
        <el-button class="btn">图书信息</el-button>
      </router-link>
      <router-link to="/cnnode">
        <el-button class="btn">CNNode论坛</el-button>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      massage: "江西软件大学-图书管理系统",
    };
  },
};
</script>

<style>
#headerTitle {
  display: inline-block;
  height: 60px;
  color: white;
  font-size: 20px;
  font-weight: bolder;
  line-height: 60px;
}
#headerFunction {
  /* display: inline-block; */
  height: 60px;
  float: right;
  line-height: 60px;
}
#headerFunction .btn {
  background-color: #0a9588;
  border-color: #0a9588;
  color: white;
  margin-left: 15px;
}
</style>