<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
      <router-link to="/contact">Contact </router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
  name :'app',

}
</script>

<style src = "../node_modules/bootstrap/dist/css/bootstrap-reboot.min.css">
#app {
  background-color:gray;
  text-align: center;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;

}
</style>

