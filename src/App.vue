<template>
  <div id="app">
    <el-row :gutter="20" class="wraper">
      <el-col :span="7" class="wraper-left">
        <leftMenu></leftMenu>
      </el-col>
      <el-col :span="17" class="wraper-left">
        <router-view/>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import leftMenu from './components/left-menu'
export default {
  name: 'App',
  components:{
    leftMenu:leftMenu
  }
}
</script>
