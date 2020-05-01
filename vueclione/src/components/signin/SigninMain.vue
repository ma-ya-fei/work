<template>
  <main>
    <section>
      <div class="signinmain">
        <div class="signinmain_left">
          <img src="../../assets/sign_portrait.jpg" alt />
        </div>
        <div class="signinmain_right">
          <div class="signinmain_right_gion">
            <div class="signinmain_right_gion_choice">
              <div class="choice_student">
                <img src="../../assets/sign_student.jpg" alt />
                <p>我是学生</p>
              </div>
              <div class="choice_lecturer">
                <img src="../../assets/sign_lecturer.jpg" alt />
                <p>我是老师</p>
              </div>
              <div class="choice_hr">
                <img src="../../assets/sign_hr.jpg" alt />
                <p>我是HR</p>
              </div>
            </div>
            <div class="signinmain_right_gion_content clearfix">
              <div class="account_login" v-show="account">
                <div class="content_mode">
                  <span
                    v-for="(item,index) in items"
                    :key="item.id"
                    @click="mode(index)"
                    :class="{color:index==current}"
                  >{{item.name}}</span>
                </div>
                <div class="content_input">
                  <form action>
                    <input class="mobile_phone" type="text" placeholder="手机号" />
                    <input class="poss_word" type="text" placeholder="密码" />
                  </form>
                </div>
                <p class="content_forget">
                  <a @click="forget(account,code)" href="javescript:;">忘记密码?</a>
                </p>
                <form action>
                  <input class="button" type="button" value="登陆了!" />
                </form>
                <p class="not">
                  还没有账号? 请
                  <a @click="not(account,mobile)" href="javescript:;">注册</a>
                </p>
              </div>
              <div class="verification_code" v-show="code">
                <div class="verification_code_login">通过手机验证码登录</div>
                <div class="content_input">
                  <form action>
                    <input class="mobile_phone" type="text" placeholder="手机号" />
                    <label for>获取验证码</label>
                    <input class="poss_word" type="text" placeholder="密码" />
                  </form>
                </div>
                <form action>
                  <input class="button" type="button" value="登陆了!" />
                </form>
              </div>
              <div class="mobile_registration" v-show="mobile">
                <div class="verification_code_login">通过手机号码注册</div>
                <div class="content_input">
                  <form action>
                    <input class="mobile_phone" type="text" placeholder="手机号" />
                    <label for>获取验证码</label>
                    <input class="poss_word" type="text" placeholder="验证码" />
                    <input class="poss_word" type="text" placeholder="密码" />
                  </form>
                </div>
                <form action>
                  <input class="button" type="button" value="提交注册" />
                </form>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>


<script>
export default {
  name: "SigninMain",
  data: function() {
    return {
      current: 0,
      account: true,
      code: false,
      mobile: false,
      items: [
        { id: "1", name: "账号登录" },
        { id: "2", name: "微信登录" }
      ]
    };
  },
  methods: {
    mode(index) {
      this.current = index;
    },
    forget(account, code) {
      this.account = !account;
      this.code = !code;
    },
    not(account, mobile) {
      this.account = !account;
      this.mobile = !mobile;
    }
  }
};
</script>

<style scoped lang="less">
//密码登录
.signinmain {
  display: flex;
}
.signinmain_right {
  position: relative;
}
.signinmain_right_gion {
  display: flex;
  position: absolute;
  width: 652px;
  height: 451px;
  top: 120px;
  left: -114px;
  border-radius: 5px;
  overflow: hidden;
}
.signinmain_right_gion_choice {
  width: 114px;
}
.signinmain_right_gion_choice div {
  padding: 30px 0px;
  text-align: center;
  color: white;
  background-color: #202421;
}
.signinmain_right_gion_choice .choice_lecturer {
  padding: 80px 0px;
  background-color: #adc700;
}
.signinmain_right_gion_content {
  flex: 1;
  padding: 0px 60px;
  background-color: white;
}
.content_mode {
  margin-top: 60px;
}
.content_mode span {
  color: #8e96a4;
  border-bottom: 2px solid #ededed;
  cursor: pointer;
}
.content_mode span:first-child {
  padding: 0px 93px 10px 60px;
}
.content_mode span:last-child {
  padding: 0px 60px 10px 93px;
}
.content_mode .color {
  color: #afc90e;
  border-bottom: 2px solid #a5c200;
}
.content_mode span:hover {
  color: #afc90e;
}
.content_input .mobile_phone {
  width: 418px;
  margin-top: 80px;
  border: 0px;
  border-bottom: 1px solid #f1f1f1;
}
.content_input .poss_word {
  width: 418px;
  margin-top: 58px;
  border: 0px;
  border-bottom: 1px solid #f1f1f1;
}
.content_forget a {
  float: right;
  color: #969dab;
  margin-top: 10px;
}
.content_forget a:hover {
  color: #434547;
}
.button {
  border: 0px;
  width: 418px;
  padding: 12px 0px;
  text-align: center;
  color: white;
  background-color: #adc700;
  border-radius: 20px;
  cursor: pointer;
  margin-top: 60px;
}
.not {
  width: 418px;
  text-align: center;
  color: #cacaca;
  margin: 24px 0px;
}
.not a {
  color: #afc90e;
}
.not a:hover {
  color: #788b08;
}
//手机登录
.verification_code_login {
  width: 418px;
  margin-top: 60px;
  padding-bottom: 10px;
  text-align: center;
  border-bottom: 2px solid #ededed;
}
.verification_code .content_input .mobile_phone {
  margin-top: 68px;
}
.content_input label {
  margin-left: -70px;
  color: #adc700;
}
.content_input label:hover {
  color: #869905;
  cursor: pointer;
}
.verification_code .button {
  margin-top: 89px;
}
//手机注册
.mobile_registration .content_input input {
  margin-top: 54px;
}
.mobile_registration .button {
  margin-top: 42px;
}
</style>