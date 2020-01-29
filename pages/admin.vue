<template>
  <div>
    <h1>Admin</h1>
    <button type="button" v-on:click="getInfo">Get INfo</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  methods: {
    mounted() {
      this.getInfo();
    },
    async getInfo() {
      console.log("GETTING INFO");
      await axios
        .get(
          `https://ldrech5yci.execute-api.us-west-2.amazonaws.com/production/api/attendees`
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

<style lang="scss" scoped>
</style>