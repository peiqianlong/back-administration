<template>
  <div class="headertop">
    <div class="hello">
      <div class="navigation" @click="Fold">
        <i class="el-icon-d-arrow-left"></i>
      </div>
      <div class="navigation">
        <i class="el-icon-goods"></i>
        <span>商城</span>
      </div>
      <div class="navigation">
        <i class="el-icon-message"></i>
        <span>邮箱</span>
      </div>
    </div>
    <div class="signout">
      <el-button type="primary">登出</el-button>
    </div>
  </div>
</template>

<script>
export default {
  name: "BackHeader",
  props: {},
  methods:{
    Fold(){
        this.$emit("flod")
    },
  }
};
</script>

<style scoped>
.headertop {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.hello {
  display: flex;
  height: 100%;
}
.navigation {
  width: 60px;
  height: 60px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}
i {
  font-size: 28px;
}
span {
  line-height: 20px;
  height: 20px;
}
</style>
