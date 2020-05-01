<template>
  <div class="conten_right">
    <div class="conter_right_my">
      <ul>
        <li v-for="info in infos" :key="info.id" class="my_thing">
          <p class="my_thing_curriculum">{{info.curriculum}}</p>
          <div class="my_thing_number">
            <div class="my_thing_number_three">
              <p class="three_individual">
                <span class="three_individual_t">{{info.t}}</span>
                <span class="three_individual_i">{{info.i}}</span>
              </p>
              <p class="three_individual_see">{{info.see}}</p>
            </div>
            <div class="my_thing_number_img">
              <img :src="info.img" alt />
            </div>
          </div>
        </li>
      </ul>
    </div>
    <div class="conter_right_sewest">
      <div class="sewest_title">
        <p class="sewest_title_student">最新学员</p>
        <p class="sewest_title_newly">一周内新增25位学员</p>
      </div>
      <ul>
        <li v-for="sewest in sewests" :key="sewest.id" class="sewest_list">
          <a href="javascript:;">
            <img class="sewest_list_img" :src="sewest.img" alt />
          </a>
          <p class="sewest_list_name">
            <a href="javascript:;">{{sewest.name}}</a>
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ConterRight",
  data: function() {
    return {
      infos: [
        {
          id: 1,
          curriculum: "我上传的课程",
          t: "3",
          i: "个",
          see: "查看详情 >",
          img: require("../../assets/curriculum.jpg")
        },
        {
          id: 2,
          curriculum: "我的问答",
          t: "3",
          i: "个",
          see: "查看详情 >",
          img: require("../../assets//ask.jpg")
        }
      ],
      sewests: [
        { id: 1, img: require("../../assets/student_1.jpg"), name: "杨志" },
        { id: 2, img: require("../../assets/student_2.jpg"), name: "杨静静" },
        { id: 3, img: require("../../assets/student_3.jpg"), name: "吕子秋" },
        { id: 4, img: require("../../assets/student_4.jpg"), name: "阎强" },
        { id: 5, img: require("../../assets/student_5.jpg"), name: "郭小宜" }
      ]
    };
  }
};
</script>

<style scoped lang="less">
.conten_right {
  flex: 1;
}
.conter_right_my ul {
  display: flex;
}
.my_thing {
  margin-left: 20px;
  padding-left: 54px;
  background-color: white;
}
.my_thing_curriculum {
  font-size: 18px;
  margin-top: 18px;
}
.my_thing_number {
  display: flex;
  margin-top: 24px;
}
.my_thing_number_three {
  margin-right: 10px;
}
.three_individual_t {
  font-size: 30px;
}
.three_individual_see {
  color: #cdcdcd;
}
.my_thing_number_img img {
  width: 260px;
  height: 181px;
}
/* 首页内容右二 */
.conter_right_sewest {
  margin-top: 16px;
  margin-left: 20px;
}
.sewest_title {
  display: flex;
  justify-content: space-between;
  padding: 24px 64px 0px 64px;
  background-color: white;
}
.sewest_title_student {
  font-size: 18px;
}
.sewest_title_newly {
  color: #cdcdcd;
}
.conter_right_sewest ul {
  display: flex;
  justify-content: space-evenly;
  background-color: white;
  text-align: center;
  padding: 26px 0px;
}
.sewest_list_img {
  width: 90px;
}
.sewest_list_name a {
  display: inline-block;
  color: #cdcdcd;
  margin-top: 6px;
}
/* 信息页面左一 */
.information_left {
  background-color: white;
  margin-right: 20px;
}
.information_left_head {
  padding: 40px 94px 117px 94px;
}
.information_left_head .head_img {
  width: 90px;
  height: 90px;
  overflow: hidden;
  position: relative;
  border-radius: 50%;
  margin-bottom: 55px;
}
.information_left_head .head_img img {
  width: 90px;
}
.information_left_head .edit {
  position: absolute;
  text-align: center;
  line-height: 25px;
  bottom: 0px;
  left: 0px;
  width: 90px;
  height: 30px;
  color: #f3efef;
  background-color: rgba(115, 110, 103, 0.5);
}
.information_left_head li {
  margin-bottom: 40px;
}
.information_left_head li i {
  padding-right: 6px;
}
.information_left_head ul li:first-child a {
  color: #00aaff;
}
</style>