<template>
  <header>
    <div class="header currency">
      <div class="header_left">
        <img class="header_left_img" src="../../assets/logo.jpg" alt />
      </div>
      <div class="header_right">
        <img class="header_right_img" src="../../assets/head_small.jpg" alt />
        <span class="header_right_name">罗密欧</span>
        <i class="fa fa-angle-down" aria-hidden="true"></i>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: "Herder"
};
</script>


<style scoped lang="less">
header{
     background-color: #333333;
}
.header{
    display: flex;
    justify-content: space-between;;
    background-color: #333333;
    color: white;
    padding: 6px 0px;
}
.header_left_img{
    height: 34px;
}
.header_right_img{
    height: 34px;
}
.header_right_name{
    display: inline-block;
    margin: 0px 10px;
}
</style>