<template>
  <div class="Signin">
    <SigninHead></SigninHead>
    <SigninMain></SigninMain>
  </div>
</template>


<script>
import SigninHead from "./SigninHead";
import SigninMain from "./SigninMain";

export default {
  name: "Signin",
  components: {
    SigninHead,
    SigninMain
  }
};
</script>

<style scoped lang="less">

</style>