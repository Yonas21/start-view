<template>
<div class="container">
  <form @submit.prevent = "addUser">
    <div class="form-group">
      <label class="label" for="userName">User Name</label>
      <input
        type="text"
        class="form-control"
        id="username"
        aria-describedby="username"
        placeholder="Enter User Name"
        v-model="skill"
      >
      <small
        id="username"
        class="form-text text-muted"
      >Your User Name is Unique.</small>
      <hr>
      <small
        class="form-text text-muted"
      >{{skill}}</small>
    </div>
    <button type="submit" class="btn btn-primary">Submit</button>
  </form>
  <ul>
    <li v-for="(data,index) in skills" :key = 'index'>{{data.text}}</li>
  </ul>
</div>
  
</template>

<script>
export default {
  name: "contact",
  data() {
    return {
      skill: '',
      skills:[
        { text: 'Front End Developer'},
        { text: 'Angular Material Design'}
      ]
    };
  },
  methods: {
    addUser(){
      this.skills.push({skill:this.skill})
      this.skill = '';
    }
  }
};
</script>

<style src = "C:/Users/Yon Real/Documents/FeedbackHub/start-vue/node_modules/bootstrap/dist/css/bootstrap.min.css">

</style>
