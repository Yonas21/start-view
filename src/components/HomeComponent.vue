
<template>
  <div id="app">
    My Name is {{ name }}.
    <hr>
    {{btnState?'button is disabled':'Button is Active.'}}
    <hr>
    <button v-bind:disabled="btnState">change Name</button>
    <p v-for="(data,index) in skills" :key = 'index'>{{data.text}}</p>
    <hr>
    <span v-if="skills.length > 2">You have more than thing you have know.</span>
    <span v-else>You need see Yourself back.</span>

    <hr/>
    <span v-if="!seen">this section is seen.</span>

    <!-- another view holder for the style -->
    <div v-bind:class="setAlarm">
      Please.
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      name: "Yonas",
      btnState: true,
      seen:false,
      skills: [
        { text: "Welcome to Android." },
        { text: "Welcome to html." },
        { text: "Welcome to JS." }
      ],
      setAlarm:{
        alert:true
      },
      skill:""
    };
  }
};
</script>

<style scoped>

button {
  color: azure;
  background-color: blueviolet;
}

.alert {
  background-color: chocolate;
  font-family:'Trebuchet MS', 'Lucida Sans Unicode', 'Lucida Grande', 'Lucida Sans', Arial, sans-serif;
  font-size: 30px;
}

.show {
  background-color: aqua;
}
</style>
