<template>
  <form>
    <form id="loginForm" @submit.prevent="handleSubmit()">
      <h1 id="checkInHeading">Check In</h1>
      <input id="nameInput" placeholder="Name" v-model="name" />
      <input id="emailInput" placeholder="Email" v-model="email" />
      <button id="checkInButton">Submit</button>
    </form>
  </form>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      name: "",
      email: ""
    };
  },
  methods: {
    async handleSubmit() {
      await axios
        .post(
          `https://ldrech5yci.execute-api.us-west-2.amazonaws.com/production/api/attendees`,
          {
            name: this.name,
            email: this.email
          }
        )
        .then(response => {
          // JSON responses are automatically parsed.
          console.log("response", response);
        })
        .catch(e => {
          this.errors.push(e);
        });
    }
  }
};
</script>

<style >
</style>