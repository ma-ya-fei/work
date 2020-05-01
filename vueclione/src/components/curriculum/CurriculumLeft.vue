<template>
  <div class="curriculum_left">
    <div class="curriculum_left_head">
      <img class="head_img" src="../../assets/head.jpg" alt />
      <div class="edit">编辑</div>
    </div>
    <ul>
      <li v-for="option in options" :key="option.id" class="head_option">
        <a href="javascript:;">
          <i class="fa" :class="option.icon"></i>
          <span>{{option.name}}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "CurriculumLeft",
  data: function() {
    return {
      options: [
        { id: 1, name: "我的课程", icon: "fa-sticky-note" },
        { id: 2, name: "我的活动", icon: "fa-shield" }
      ]
    };
  }
};
</script>

<style scoped lang="less">
.curriculum_left {
  width: 294px;
  height: 576px;
  padding: 50px 92px 0px 92px;
  margin-right: 20px;
  background-color: white;
  box-sizing: border-box;
}
.curriculum_left_head {
  width: 100px;
  height: 100px;
  overflow: hidden;
  position: relative;
  border-radius: 50%;
  margin-bottom: 50px;
}
.curriculum_left_head .head_img {
  width: 100px;
}
.curriculum_left_head .edit {
  position: absolute;
  text-align: center;
  line-height: 25px;
  bottom: 0px;
  left: 0px;
  width: 1000px;
  height: 30px;
  color: #f3efef;
  background-color: rgba(115, 110, 103, 0.5);
}
.curriculum_left li {
  margin-bottom: 40px;
}
.curriculum_left li i {
  padding-right: 6px;
}
.curriculum_left ul li:first-child a {
  font-style: 16px;
  color: #00aaff;
}
</style>