<template>
  <div class="container">
    <form @submit.prevent="addUser">
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
        <small id="username" class="form-text text-muted">Your User Name is Unique.</small>
        <hr>

		<transition name="alert-in">
			<small class="form-text text-muted">{{skill}}</small>
        </transition>

        <input type="checkbox" name="check" id="check" class="checkbox" v-model="checked"> Male
      </div>

      <button type="submit" class="btn btn-primary">Submit</button>

    </form>
    <ul>
      <li v-for="(data,index) in skills" :key="index">{{data.text}}</li>
    </ul>
  </div>
</template>

<script>
/*eslint-disable */
export default {
  name: "contactComponent",
  data() {
    return {
      checked: false,
      skill: "",
      skills: [
        { text: "Front End Developer" },
        { text: "Angular Material Design" }
      ]
    };
  },
  methods: {
    addUser() {
      if (this.skill.length <= 5) {
        console.log("You Should Enter At Least 5 Characters.");
      } else if (this.skill.length >= 20) {
        console.log("Avoid too Long Character and make it declarative");
      } else {
        this.skills.push({ text: this.skill });
        this.skill = "";
      }
      console.log("this value is " + this.checked);
    }
  }
};
</script>

<style src = "C:/Users/Yon Real/Documents/FeedbackHub/start-vue/node_modules/bootstrap/dist/css/bootstrap.min.css">

.alert-in-enter-active {
	animation-delay: bounce-in 1s
}
.alert-in-leave-active {
	animation-delay: bounce-in 1s reverse;
}

@keyframes bounce-in {
	0% {
		transform: scale(0)
	}
	50% {
		transform: scale(2)
	}
	100% {
		transform: scale(1)
	}
}
</style>
