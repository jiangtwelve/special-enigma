<template>
  <div id="left-menu">
    <div class="left-logo">
      <div class="logo" v-if="LogoShow">
        <img src='../assets/img/a6db8c2397dda1443215a30dbfb7d0a20cf4867a.jpg' >
        <p>{{ LogoName }}</p>
      </div>
      <div class="logo" v-else>
        <el-button type="primary" size="small">登录</el-button>
      </div>
    </div>
    <el-menu default-active="1" class="el-menu-vertical-demo" @open="handleOpen" @close="handleClose" background-color="#fafafa"
      text-color="#33333394" active-text-color="#333" align='center'>
      <el-menu-item index="1">
        <span slot="title">首页</span>
      </el-menu-item>
      <el-menu-item index="2">
        <span slot="title">时间记录本</span>
      </el-menu-item>
      <el-menu-item index="3">
        <span slot="title">Tudu Lists</span>
      </el-menu-item>
      <el-menu-item index="4">
        <span slot="title">个人简历</span>
      </el-menu-item>
    </el-menu>
  </div>
</template>
<script>
  export default {
    name: 'left-menu',
    data(){
      return{
        LogoImg:'../assets/img/a6db8c2397dda1443215a30dbfb7d0a20cf4867a.jpg',
        LogoName:'不喝百事江十二',
        LogoShow:true
      }
    },
    methods: {
      handleOpen(key, keyPath) {
        console.log(key, keyPath);
      },
      handleClose(key, keyPath) {
        console.log(key, keyPath);
      }
    }
  }

</script>
<style scoped>
  #left-menu {
    background-color: #fafafa;
    display: flex;
    flex-direction:column
  }
  .left-logo {
    border-right: solid 1px #e6e6e6;
    list-style: none;
    position: relative;
    margin: 0;
    padding-left: 0;
    height: 40%;
  }
  #left-menu .el-menu{
    flex-grow:1
  }
  #left-menu .left-logo .logo{
    width: 200px;
    height: 200px;
  }
  #left-menu .left-logo{
    display: flex;
    align-content: center;
    align-items: center;
    justify-content: center;
    text-align: center;
  }
  .logo img{
    width: 150px;
    height: 150px;
    border-radius: 50%;
  }
  .logo p{
    font-size: 16px;
    padding-top: 5px;
    font-weight: 400
  }
</style>
