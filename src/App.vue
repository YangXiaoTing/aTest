<template>
  <div id="app">
    <navbar></navbar>
    <div class="page-content">
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </div>
  </div>
</template>

<script>
  import checkLogin from '@/assets/js/checkLogin'
  import {Input, Button, Loading} from 'element-ui'
  import Vue from 'vue'
  Vue.use(Input)
  Vue.use(Button)
  Vue.use(Loading)

  const Navbar = r => require.ensure([], () => r(require('./components/Navbar.vue')), 'jsGroup-Navbar')
  export default {
    name: 'app',
    components: {
      Navbar
    },
    async beforeCreate () {
      let appLoading = Loading.service({
        fullsreen: true,
        customClass: 'loading',
        text: '正在初始化 ...'
      })
      await checkLogin()
      appLoading.close()
    }
  }
</script>

<style>
  @import '../static/css/blue.css';
  html{
    height: 100%;
    box-sizing: border-box;
  }
  body {
    box-sizing: border-box;
    height: 100%;
    margin: 0;
    color: #2c3e50;
    /*background: #143d5f;*/
  }

  #app {
    box-sizing: border-box;
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }

  .page-content {
    box-sizing: border-box;
    padding-top: 50px;
    color: #fff;
    font-size: 14px;
  }
  .loading{
    width: 25%;
    height: 25%;
    position: fixed;
    left:50% !important;
    top:50% !important;
    transform: translate(-50%, -50%);
    -ms-transform: translate(-50%, -50%);
    background: #222 !important;
    opacity:0.8;
    border-radius: 20px;
  }
</style>
