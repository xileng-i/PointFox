<template>
  <div id="mainWrapper">
    <div id="mainContent">
      <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>用户注册</span>
        
      </div>
      <div id="loginContent">
        <el-input id="username" v-model="newuser.username"  clearable></el-input>
        
        <el-input id="password" v-model="newuser.password"  clearable show-password></el-input>
      </div>
      <div id="submitContent">
        <el-button id="sysBut">注册</el-button>
      </div>

    </el-card>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      newuser:{
        username:"",
        password:"",
      }
    }
  }
};
</script>

<style>
#mainWrapper {
  /* background-color: pink; */
  padding-top: 40px;
}
#mainContent{
  width: 400px;
  margin: 40px auto;
}
#password{
  margin-top: 10px;
}
#sysBut{
  display: block;
  background-color: #0a9588  !important;
  border-color: #0a9588  !important;
  color: white  !important;
  margin: 0% auto  !important;
  margin-top: 15px !important;
}
</style>