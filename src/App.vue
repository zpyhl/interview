<template>
  <div id="app">
    <cnHeader></cnHeader>

    <!-- 开发的时候有时候会遇到一种情况，比如 ：点击这个链接跳转到其他组件的情况，通常会跳转到新的页面，
    蛋是，我们不想跳转到新页面，只在当前页面切换着显示，那么就要涉及到路由的嵌套了，也可以说是子路由的使用。-->
    <router-view name="main"></router-view>
    <router-view name="sidebar"></router-view>
  </div>
</template>

<script>
import cnHeader from "./components/Header";

export default {
  name: "app",
  components: {
    cnHeader
  }
};
</script>

<style>
html {
  background-color: #dddddd;
}
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  font-size: 20px;
}
body,
div,
span,
a,
p,
ul,
li {
  margin: 0;
  padding: 0;
}
</style>
