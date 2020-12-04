<template>
  <div id="app">
    <div id="backGround">
      <!-- <img src="./assets/backGround.png" width="100%" height="100%" alt="backGround" /> -->
      <img :src="imgSrc" width="100%" height="100%" alt="backGround" />
    </div>
    <div id="YelTop">
      <YelHead msg="Welcome to YEL App" />
    </div>
    <div id="YelLeft"></div>
    <div id="YelRight"></div>
    <div id="YelDown">Copyright©top.hongzhangming 版权所有，盗版必究</div>
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
      imgSrc: require("./assets/backGround.png"),
    };
  },
};
</script>

<style>
/* @import "./css/App.css"; */
@import url(./css/App.css);

#background {
  position: absolute;
  z-index: -1;
  /* width: 100%; */
  /* height: 100%; */
}

#YelTop {
  position: absolute;
  z-index: 1;
  top: 0%;
  /* background-color: rgb(104, 104, 105); */
  width: 100%;
  height: 9%;
}
#YelLeft {
  position: absolute;
  z-index: 1;
  left: 0%;
  top: 9%;
  width: 77%;
  height: 98.2%;
  background-color: rgb(212, 199, 78);
}
#YelRight {
  position: absolute;
  z-index: 1;
  right: 0%;
  top: 9%;
  width: 23%;
  height: 98.2%;
  background-color: rgb(21, 135, 189);
}
#YelDown {
  position: absolute;
  z-index: 1;
  width: 100%;
  height: 3%;
  top: 107.2%;
  background-color: rebeccapurple;
}
</style>
