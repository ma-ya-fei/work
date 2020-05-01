<template>
  <nav>
    <div class="nav currency">
      <div class="nav_left">
        <a href="javascript:;">My Conter</a>
      </div>
      <div class="nav_list">
        <ul>
          <li
            v-for="(item,index) in items"
            :key="item.id"
            :class="{bg:index==isactive}"
            @click="list_fn(index)"
          >
            <a href="javascript:;">{{item.option}}</a>
          </li>
        </ul>
      </div>
      <div class="nav_right">
        <a href="javascript:;">+ 添加课程</a>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "Nav",
  data: function() {
    return {
      isactive: -1,
      state: true,
      items: [
        { id: 1, option: "基本信息" },
        { id: 2, option: "课程管理" },
        { id: 3, option: "我的问答" },
        { id: 4, option: "我的收入" }
      ]
    };
  },
  methods: {
    list_fn(index) {
      this.isactive = index;
    }
  }
};
</script>


<style scoped lang="less">
nav {
  background-color: white;
  box-shadow: 0px 2px 1px #e1e1e1;
}
.nav {
  display: flex;
  padding: 32px 0px;
}
.nav_left a {
  display: inline-block;
  font-size: 24px;
  height: 32px;
  color: #0093ff;
  margin-right: 96px;
}
.nav_list ul {
  height: 32px;
  display: flex;
  line-height: 38px;
}
.bg a {
  color: #30baff;
  padding-bottom: 20px;
  border-bottom: 1px solid #1db4ff;
}
.nav_list ul li {
  margin-right: 90px;
}
.nav_right {
  height: 32px;
  padding: 0px 32px;
  margin-left: auto;
  border: 1px solid #f3f3f3;
  border-radius: 20px;
  line-height: 32px;
}
.nav_right a {
  color: #1db4ff;
}
</style>