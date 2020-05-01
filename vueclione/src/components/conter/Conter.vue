<template>
  <div class="conter currency">
    <ConterLeft></ConterLeft>
    <ConterRight></ConterRight>
  </div>
</template>

<script>
import ConterLeft from "./ConterLeft.vue";
import ConterRight from "./ConterRight.vue";

export default {
  name: "Conter",
  components: {
    ConterLeft,
    ConterRight
  }
};
</script>

<style scoped lang="less">
.conter {
  display: flex;
  margin-top: 30px;
}
</style>