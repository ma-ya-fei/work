<template>
  <div class="conter_left">
    <div class="conter_left_introduce">
      <div class="introduce_left">
        <a href="javascript">
          <img class="introduce_left_img" src="../../assets/head.jpg" alt />
        </a>
      </div>
      <div class="introduce_right">
        <div class="introduce_right_name">
          <span class="introduce_right_name_n">罗密欧</span>
          <img class="introduce_right_name_img" src="../../assets/head_.jpg" alt />
        </div>
        <div class="introduce_right_complete">
          <span class="introduce_right_complete_degree">信息完整度</span>
          <span class="introduce_right_complete_line"></span>
          <span class="introduce_right_complete_h">高</span>
        </div>
        <div class="introduce_right_icon">
          <i class="fa fa-lg fa-mobile fa-inverse" aria-hidden="true"></i>
          <i class="fa fa-id-card-o" aria-hidden="true"></i>
          <i class="fa fa-envelope-o" aria-hidden="true"></i>
        </div>
      </div>
    </div>
    <div class="conter_left_apply">
      <div class="apply_left">申请提现</div>
      <div class="apply_right">
        <p class="apply_right_account">账户余额</p>
        <p class="apply_right_price">
          <span class="apply_right_price_number">248</span>
          <span class="apply_right_price_element">元</span>
        </p>
      </div>
    </div>
    <div class="conter_left_attestation">
      <ul>
        <li v-for="attestation in attestations" :key="attestation.id" class="attestation_left">
          <a href="javascript:;">
            <img :src="attestation.img" alt class="attestation_left_img" />
          </a>
          <p class="attestation_left_P">
            <span class="attestation_left_P_realname">{{attestation.realname}}</span>
            <span class="attestation_left_P_not">{{attestation.not}}</span>
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: "ConterLeft",
  data: function() {
    return {
      attestations: [
        {
          id: 1,
          img: require("../../assets/realname.jpg"),
          realname: "实名认证",
          not: "【未认证】"
        },
        {
          id: 2,
          img: require("../../assets/qualifications.jpg"),
          realname: "资质认证",
          not: "【未认证】"
        }
      ]
    };
  }
};
</script>

<style scoped lang="less">
.conter_left {
  width: 468px;
  height: 576px;
  box-sizing: border-box;
  background-color: white;
}
.conter_left_introduce {
  display: flex;
  padding: 30px 0px 30px 36px;
  border-bottom: 2px solid #f4f4f4;
}
.introduce_left_img {
  width: 95px;
  margin-right: 35px;
}
.introduce_right_name {
  margin-bottom: 18px;
}
.introduce_right_name_n {
  font-weight: bold;
  margin-right: 10px;
}
.introduce_right_name_img {
  width: 18px;
}
.introduce_right_complete {
  font-size: 12px;
  margin-bottom: 12px;
}
.introduce_right_complete_degree {
  color: #676767;
  margin-right: 10px;
}
.introduce_right_complete_line {
  display: inline-block;
  padding: 3px 76px;
  background-color: #00a3ff;
  border-radius: 10px;
  margin-right: 10px;
}
.introduce_right_complete_h {
  color: #70cfff;
}
.fa-inverse {
  color: blue;
}
/* 首页内容左二 */
.conter_left_apply {
  display: flex;
  margin-top: 2px;
  padding: 30px 0px 30px 36px;
  align-items: center;
  border-bottom: 2px solid #f4f4f4;
}
.apply_left {
  color: white;
  height: 30px;
  line-height: 30px;
  margin-right: 54px;
  padding: 0px 55px;
  background-color: #00aaff;
  border-radius: 20px;
}
.apply_right_account,
.apply_right_price_element {
  font-size: 12px;
  color: #8d8d8d;
}
.apply_right_account {
  margin-bottom: 12px;
}
.apply_right_price_number {
  font-size: 24px;
  font-weight: bold;
}
/* 首页内容左三 */
.conter_left_attestation {
  padding: 64px 36px;
}
.conter_left_attestation ul {
  display: flex;
}
.conter_left_attestation ul li {
  margin-right: 35px;
  text-align: center;
}
.attestation_left_img {
  margin-bottom: 12px;
}
.attestation_left_P_realname {
  color: #9b9b9b;
}
.attestation_left_P_not {
  color: red;
}
/* 首页内容右一 */
.conter_right_my {
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