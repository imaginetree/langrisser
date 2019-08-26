<template>
  <div id="app">
    <el-tabs v-model="activeName" @tab-click="handleClick">
      <el-tab-pane label="Home" name="home"></el-tab-pane>
      <el-tab-pane label="About" name="about"></el-tab-pane>
    </el-tabs>
    <router-view/>
  </div>
</template>
<script>
  export default {
    data() {
      return {
        activeName: 'first'
      };
    },
    methods: {
      handleClick(tab) {
        console.log(tab.name);
         this.$router.push(tab.name);
      }
    }
  };
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
  margin-left: 20px;
}
</style>
