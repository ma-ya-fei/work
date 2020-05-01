<template>
  <div class="curriculum_right">
    <div class="curriculum_right_list">
      <form>
        <input id="release" type="radio" name="state" checked/>
        <label for="release">已发布课程</label>
        <input id="ongoing" type="radio" name="state"/>
        <label for="ongoing">审核中课程</label>
        <input id="fail" type="radio" name="state"/>
        <label for="fail">未通过审核课程</label>
      </form>
    </div>
    <div class="curriculum_right_video">
      <div class="video_one">
        <div class="video_one_left">
          <img src="../../assets/release_1.jpg" alt />
        </div>
        <div class="video_one_right">
          <p class="video_one_right_title">
            <span>显露你实力的一面</span>
            <span>进行中</span>
          </p>
          <p class="video_one_right_time">上传时间: 3月23日 15:43</p>
          <p class="video_one_right_num">
            <span>
              <i class="fa fa-user" aria-hidden="true"></i>128位学员
            </span>
            <span>
              <i class="fa fa-commenting" aria-hidden="true"></i>18条评论
            </span>
          </p>
          <p class="video_one_right_price">免费</p>
        </div>
      </div>
      <div class="video_one">
        <div class="video_one_left">
          <img src="../../assets/release_2.jpg" alt />
        </div>
        <div class="video_one_right">
          <p class="video_one_right_title">
            <span>微信微博新媒体营销课程</span>
            <span>已结束</span>
          </p>
          <p class="video_one_right_time">上传时间: 3月23日 15:43</p>
          <p class="video_one_right_num">
            <span>
              <i class="fa fa-user" aria-hidden="true"></i>128位学员
            </span>
            <span>
              <i class="fa fa-commenting" aria-hidden="true"></i>18条评论
            </span>
          </p>
          <p class="video_one_right_price">￥199</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CurriculumRight"
};
</script>

<style scoped lang="less">
.curriculum_right {
  flex: 1;
  background-color: white;
}
.curriculum_right_list {
  padding: 40px 0px 40px 30px;
}
.curriculum_right_list input{
  width: 30px;
  height: 30px;
  vertical-align: middle;
}
.curriculum_right_list label {
  margin-right: 50px;
}
.video_one {
  display: flex;
  padding: 40px 0px 40px 30px;
  border-top: 1px solid #f3f3f3;
}
.video_one_left {
  margin-right: 20px;
}
.video_one_right_title span:first-child {
  font-size: 18px;
  margin-right: 20px;
}
.video_one_right_title span:last-child {
  font-size: 18px;
  color: #00a6ff;
}
.video_one_right p {
  margin-bottom: 14px;
  cursor: pointer;
}
.video_one_right_time,
.video_one_right_num {
  color: #cbcbcb;
}
.video_one_right_num span:first-child {
  margin-right: 10px;
}
.video_one_right .video_one_right_price {
  font-size: 18px;
  color: #00a6ff;
  margin-bottom: 0px;
}
</style>