<template>
  <div id="app">
    <!-- <img src="./assets/backGround.png" width="100%" height="100%" alt="backGround" /> -->
    <!-- <img :src="imgSrc" width="100%" height="100%" alt="backGround" /> -->
    <div id="YelTop">
      <YelHead msg="www.hongzhangming.top" />
    </div>
    <div id="YelBody">
      <div id="YelLeft"></div>
      <div id="YelRight"></div>
    </div>

    
    <div id="YelDown">
      <span style="font-size: 12px"
        >Copyright © top.hongzhangming 版权所有，侵权必究</span
      >
    </div>

  </div>
</template>

<script>
import YelHead from "./components/YelHead.vue";

export default {
  name: "App",
  components: {
    YelHead,
  },
  data() {
    return {
      imgSrc: require("./assets/logo.png"),
    };
  },
};
</script>

<style>
/* @import "./css/App.css"; */
@import url(./css/App.css);

</style>
