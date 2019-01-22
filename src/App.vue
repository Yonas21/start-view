<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="set to do something."/>
    <div id = "about">
      <about msg="seen if true."/>
    </div>
  </div>
</template>


<script>
import HelloWorld from './components/HelloWorld.vue'
import about from './components/About.vue';
/* eslint-disable */
export default {
  name: 'app',
  components: {
    HelloWorld,
    about
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
