<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <hr>
    <p>Coniditonal Statements</p>
    <span v-if="seen">Visible if True.</span>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data:{
    seen:true
  },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

span {
  color: aqua;
  font-size: 20px;
}
a {
  color: #42b983;
}
</style>
