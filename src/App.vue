<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <div>
      <button @click="getApiData">POST Data to API</button>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "App",
  components: {},
  methods: {
    async getApiData() {
      var payload = {
        app_name: "prodfda",
        uid: "some uid2",
        token:
          "e1gPO7MNT8qzm_Fs2Ny17g:APA91bF1CXKkLU3sI9KeW8pW7g-dYmOzqQzDgcOMbiYdiIm2zpmsv3cUS7ZF7byW-s5HITt2GB7L5rVH_ncGRxwRhUGOXEGKxtPtZQGQnWlX_cCourmrONqQ6XIf9PYDWjQM3aMRp-Xw",
        email: "test123@grr.la",
      };
      console.log("notification payload", payload);
      var response = await axios.post(
        `https://notificationservice.in/fcm/register`,
        payload
      );
      console.log(response.data);
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
