<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld class="font-bold text-2xl" msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import axios from "axios";

export default {
  name: "HomeView",
  components: {
    HelloWorld,
  },
  mounted() {
    axios
      .get("http://localhost:3000/foo")
      .then(function (response) {
        // handle success
        console.log(response.data.msg);
      })
      .catch(function (error) {
        // handle error
        console.log(error);
      });
  },
};
</script>
