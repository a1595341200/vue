<template>
  <div class="app">
    <div class="b1">
      <div class="b2">
        <router-link to="/home">Home </router-link>
      </div>
      <div class="b3">
        <router-link to="/about">About</router-link>
      </div>
    </div>
    <router-view></router-view>
  </div>
</template>
<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #071f36;
  letter-spacing: 1px;
  font-family: "Helvetica Neue", Helvetica, "PingFang SC", "Hiragino Sans GB", "Microsoft YaHei", "微软雅黑", Arial, sans-serif;
}

body {
  margin: 0px;
}

#container {
  position: relative;
  margin-right: auto;
}

::selection {
  background: #96c7c9;
  /* Safari */
  color: #ffffff;
}

::-moz-selection {
  background: #8fbbb9;
  /* Firefox */
  color: #ffffff;
}

.b1 {
  width: 600px;
  background-color: royalblue;
  overflow: hidden;
  position: relative;
}

.b2 {
  width: 150px;
  height: 80px;
  /* background-color: red; */
  background-color: royalblue;
  float: left;

}

.b3 {
  width: 150px;
  height: 60px;
  /* background-color: chartreuse; */
  background-color: royalblue;
  float: right;
  margin: auto 0 auto auto;
  /*  上右下左  */
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;

}

@media screen and (max-width:768px) and (min-width: 100px) {
  .nav {
    display: none;
  }

  .changeStyle {
    font-weight: bold;
  }

  .nav-image {
    float: left;
    display: inline;
    margin-top: 10px;
    margin-left: 30px;
  }

  .nav-search {
    float: left;
    margin-left: 28%;
    margin-top: 23px;
  }

  .el-icon-message {
    margin-left: 70px;
    cursor: pointer;
  }

  .github-corner {
    display: none;
  }
}

@media screen and (max-width: 3000px) and (min-width: 767px) {
  .navs {
    width: 100%;
    height: 80px;

    /* line-height: 80px; */
    .nav {
      float: left;
      margin-left: 40px;
      font-size: 18px;
      cursor: pointer;
      margin-top: 30px;
    }

    .changeStyle {
      font-weight: bold;
    }

    .nav-image {
      float: left;
      display: inline;
      margin-top: 10px;
      margin-left: 17%;
    }

    .nav-search {
      float: left;
      margin-left: 15px;
      margin-top: 23px;
      cursor: pointer;
    }

    .el-icon-message {
      margin-left: 400px;
      cursor: pointer;
    }
  }
}
</style>
