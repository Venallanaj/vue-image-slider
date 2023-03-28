<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <AppSlider />
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from "@/components/HelloWorld.vue";
import AppSlider from "@/components/AppSlider.vue";

export default {
  name: "HomeView",
  components: {
    // HelloWorld,
    AppSlider,
  },
};
</script>
