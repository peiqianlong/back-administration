<template>
  <div class="hello">
    <div class="logo">Logo</div>
    <el-menu
      default-active="2"
      class="el-menu-vertical-demo"
      @open="handleOpen"
      @close="handleClose"
      background-color="#545c64"
      text-color="#fff"
      active-text-color="#ffd04b"
      router
      collapse = sasidewidth
    >
      <el-submenu index="1" style=width:200px>
      <!-- <el-submenu index="1" style=" width : {isasidewidth ? '70px' : '200px'}"> 
      collapse = isasidewidth -->
        <template slot="title" >
          <i class="el-icon-location"></i>
          <span>导航一</span>
        </template>
        <el-menu-item-group>
          <el-menu-item index="/about">选项1</el-menu-item>
          <el-menu-item index="/home">选项2</el-menu-item>
        </el-menu-item-group>
      </el-submenu>
    </el-menu>
  </div>
</template>

<script>
export default {
  name: "BackAside",
  props: {
      isasidewidth:{
        type:Boolean,
        value:false
      }
  },
  methods: {
    handleOpen(key, keyPath) {
    },
    handleClose(key, keyPath) {
    }
  }
};
</script>

<style scoped>
.logo {
  width: 100%;
  height: 60px;
  color:white;
  line-height: 60px;
}
</style>
