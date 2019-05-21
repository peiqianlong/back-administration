<template>
  <div id="app"  v-cloak>
    <!-- <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view/>-->

    <el-container style="height:100%;">
      <el-aside class="styleone"  :style="{width : asidewidth }">
          <BackAside :isasidewidth = isasidewidth></BackAside>
      </el-aside>
      <el-container>
        <el-header>
           <BackHeader @flod = "flod"></BackHeader>
        </el-header>
        <el-main><router-view/></el-main>
      </el-container>
    </el-container>
  </div>
</template>
<script>
import BackAside from "./components/BackAside"
import BackHeader from "./components/BackHeader"
export default {
  name: "app",
  components: {
      BackAside,
      BackHeader
  },
  data(){
    return({
      asidewidth:"200px",
      isasidewidth:false,
    })
  },
  methods:{
    flod(){
        if(this.asidewidth === "200px"){
          this.asidewidth = "70px"
          this.isasidewidth = true
        }else{
          this.asidewidth = "200px"
          this.isasidewidth = false
        }
    }
  }
};
</script>
<style scoped>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}
.el-header, .el-footer {
    background-color: #B3C0D1;
    color: #333;
    text-align: center;
    line-height: 60px;
  }
  
  .el-aside {
    background-color: #D3DCE6;
    color: #333;
    text-align: center;
    line-height: 200px;
  }
  
  .el-main {
    background-color: #E9EEF3;
    color: #333;
    text-align: center;
    line-height: 160px;
  }
  
  body > .el-container {
    margin-bottom: 40px;
  }
  
  .el-container:nth-child(5) .el-aside,
  .el-container:nth-child(6) .el-aside {
    line-height: 260px;
  }
  
  .el-container:nth-child(7) .el-aside {
    line-height: 320px;
  }
  .styleone{
    width:200px;
    background-color:rgb(84, 92, 100)
  }
</style>
