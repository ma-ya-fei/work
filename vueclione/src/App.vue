<template>
  <div id="app">
    <!-- <Signin></Signin> -->
    <Sccess></Sccess>
  </div>
</template>

<script>
// import Signin from "./components/signin/Signin.vue";
import Sccess from "./components/sccess/Sccess.vue";

export default {
  name: "App",
  components: {
    // Signin,
    Sccess
  }
};
</script>

<style lang="less">
#app {
  background-color: #f4f4f4;
}
.currency {
  width: 1260px;
  margin: 0 auto;
}
</style>
