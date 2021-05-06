<template>
  <div id="app">
    <el-container>
<!-- 3、使用组件 -->
      <el-header id="headerBook"><Header/></el-header>
      <el-main id="mainBook">
        <div id="mainBookWrapper">
          <router-view>

          </router-view>
        </div>
        </el-main>
      <el-footer id="footerBook"><Footer/></el-footer>
    </el-container>
  </div>
</template>

<script>
//1、导入组件
import Header from'./components/Header.vue';
import Footer from'./components/Footer.vue';
// import Main from'./components/Main.vue';

// import CNNode from'./components/CNNode.vue';
// import Book from './components/Book.vue';
// import Reader from './components/Reader.vue';
// import Work from './components/Work.vue';
// import Register from './components/Register.vue';


export default {
  name: "App",
//2、注册组件
  components: {
    Header,
    Footer,
    // Main,
    
    // CNNode,
    // Work,
    // Book,
    // Reader,
    // Register
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
}

#headerBook{
  background-color:#244152;
}

/* #mainBook{
 background-color: yellow; 

}

#footerBook{
   background-color: pink; 
} */
#mainBookWrapper{
  height: 450px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  /* margin-top: 60px; */
  
}
</style>
