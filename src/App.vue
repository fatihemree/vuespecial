<template>
  <div id="app">
    <el-container>
      <el-header>    <HelloWorld></HelloWorld>  </el-header>
      <el-main> <vuelist></vuelist>  </el-main>
    </el-container>

  </div>
</template>

<script>
  import HelloWorld from './components/HelloWorld.vue'
  import vuelist from './components/list.vue'

  export default {
    name: 'app',
    components: {
      HelloWorld,
      vuelist
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
