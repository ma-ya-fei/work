<template>
  <header>
    <div class="signinhead">
      <div class="signinhead_left">
        <img class="signinhead_left_img" src="../../assets/sign_logo.jpg" alt />
      </div>
      <div class="signinhead_right">
        <a href="javascript:;">
          <span @click="not(account,mobile)">注册</span>
        </a> |
        <a href="javascript:;">
          <span>登录</span>
        </a>
      </div>
    </div>
  </header>
</template>


<script>
export default {
  name: "SigninHead"
};
</script>

<style scoped lang="less">
header {
  background-color: white;
}
.signinhead {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 15px 150px 15px 120px;
}
.signinhead_right,
.signinhead_right a {
  color: #a0a0a0;
}
.signinhead_right a:hover {
  color: #5d5d5d;
}
</style>