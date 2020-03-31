<template>
  <div id="main-app">
    <!-- loading -->
    <div v-if="loading">loading</div>
    <div>
      <div id="nav">
        <a href="/app1">子项目1</a>
        <a href="/app2">子项目2</a>
      </div>
      <!-- 子应用盒子 -->
      <div id="root-view" class="app-view-box" v-html="content"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  props: {
    loading: Boolean,
    content: String
  }
};
</script>

<style>
#main-app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  margin-right: 20px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.app-view-box {
  margin-left: 200px;
  border-top: 1px solid gray;
  border-left: 1px solid gray;
}
</style>
