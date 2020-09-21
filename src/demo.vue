<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
<!--   <svg-animation></svg-animation>-->
<!--    <test-component2></test-component2>-->
<!--    <test-component3></test-component3>-->
<!--    <yLoading-->
<!--      width="100"-->
<!--      height="100"-->
<!--      duration="2"-->
<!--    >-->
<!--      加载中...-->
<!--    </yLoading>-->
    <y-fly-box
      style="width: 50%;background: #333;color:#fff"
    >
        <div>dsds</div>
    </y-fly-box>

    <y-fly-box
      style="width: 100%;background: #333;color:#fff"
    >
      <div>dsds</div>
    </y-fly-box>

    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
