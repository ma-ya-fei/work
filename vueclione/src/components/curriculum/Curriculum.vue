<template>
  <div class="curriculum currency">
    <CurriculumLeft></CurriculumLeft>
    <CurriculumRight></CurriculumRight>
  </div>
</template>

<script>
import CurriculumLeft from "./CurriculumLeft.vue";
import CurriculumRight from "./CurriculumRight.vue";
export default {
  name: "Curriculum",
  components: {
    CurriculumLeft,
    CurriculumRight
  }
};
</script>

<style scoped lang="less">
.curriculum {
  display: flex;
  margin-top: 30px;
}
</style>