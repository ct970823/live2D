<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld/>
    
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import cityArr from '../static/city';
export default {
  name: 'App',
  data(){
    return {
      cityArr:cityArr.cityArr
    }
  },
  components: {
    HelloWorld
  },
  created(){
    // this.getArr()
    setTimeout(()=>{
      window.L2Dwidget.init({
      pluginRootPath: 'live2dw/',
      pluginJsPath: 'lib/',
      pluginModelPath: 'live2d-widget-model-z16/assets/',
      tagMode: false,
      debug: false,
      model: { jsonPath: '../static/live2dw/live2d-widget-model-shizuku/assets/shizuku.model.json' },//资源文件
      display: { position: 'right', width: 200, height: 400 },//尺寸与位置
      mobile: { show: true },//跟随鼠标
      log: true
    })
    },1000)
  },
  methods:{
    
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
