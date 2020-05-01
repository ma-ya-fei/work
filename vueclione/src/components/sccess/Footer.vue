<template>
  <footer>
    <div class="footer currency">
      <p class="footer_c">
        <span>中国领先大学生平台</span>
        <span>2016 e学聘</span>
      </p>
      <p>
        <span>ICP备 16500007号 |</span>
        <a href="javascript:;">联系我们</a>
        <span>exuepin@exuepin.com |</span>
        <a href="javascript:;">关于我们</a>
      </p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer"
};
</script>


<style scoped lang="less">
footer{
  background-color: white;
}
.footer{
    margin-top: 30px;
    text-align: center;
    padding: 28px 0px 24px 0px;
}
.footer .footer_c{
    margin-bottom: 6px;
}
.footer p a,
.footer p span{
    color: #9b9b9b;
    margin-right: 6px;
}
</style>