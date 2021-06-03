<template>
  <div id="mainWrapper">
    <div id="mainContent">
      <el-card class="box-card">
      <div slot="header" class="clearfix">
        <span>用户注册</span>
        
      </div>
      <div id="loginContent">
        <el-input id="newusername" v-model="newUser.newusername"  clearable></el-input>
        
        <el-input id="newpassword" v-model="newUser.newpassword"  clearable show-password></el-input>
      </div>
      <div id="submitContent">
        <el-button id="sysBut"  @click="registerSystem" >注册</el-button>
      </div>

    </el-card>
    </div>
  </div>
</template>

<script>
import Axios from 'axios'
const url = 'http://localhost:3000'


export default {
  data(){
    return {
            newUser:{
                newusername:"",
                newpassword:""
            },
            fullscreenLoading: false
        }
  },
  methods:{
    registerSystem(){

      Axios.get(url+'/register',{params:this.newUser}).then((resx)=>{
        if(resx.data.state=="success"){
          this.$message(resx.data.message)
        }
      })
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
#newpassword{
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