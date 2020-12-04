<template>
  <div class="yelHead">
    <div>
      <h2 id="homeText" v-on:click="toHome">
        {{ msg }}
      </h2>
    </div>
    <div style="position: fixed; right: 0%; top: 25%">
      <input
        type="text"
        v-model="searchKey"
        id="searchKey"
        placeholder="搜索框"
      /><br />
      <button v-on:click="search" disabled="false">本站搜索</button><br />
      <button v-on:click="bySearch">必应</button><br />
      <button v-on:click="byTranslation">必应词典</button><br />
      <button v-on:click="bdSearch">百度</button><br />
      <button v-on:click="bdTranslation">百度翻译</button><br />
    </div>
    <div style="position: fixed; right: 3%; top: 0%">
      <img src="../assets/logo.png" alt="头像" title="headImg" id="headImg" />
      <!-- {{ fullname }} -->
    </div>
    <div id="qqChat">
      <a
        target="_blank"
        href="http://wpa.qq.com/msgrd?v=3&uin=1121508290&site=qq&menu=yes"
        ><img
          src="http://wpa.qq.com/pa?p=2:1121508290:51"
          alt="联系开发者"
          title="联系开发者"
      /></a>
    </div>
  </div>
</template>

<script>
export default {
  name: "YelHead",
  props: {
    msg: String,
  },
  data() {
    return {
      fullname: "游客",
      searchKey: "",
    };
  },
  methods: {
    toHome: function () {
      // window.location.href = "http://www.hongzhangming.top";
      window.location.reload();
    },
    search: function () {
      alert("功能未开发！");
    },
    bdSearch: function () {
      window.open("https://www.baidu.com/s?wd=" + this.searchKey);
    },
    bdTranslation: function () {
      window.open("https://fanyi.baidu.com/#zh/en/" + this.searchKey);
    },
    bySearch: function () {
      window.open("https://cn.bing.com/search?q=" + this.searchKey);
    },
    byTranslation: function () {
      window.open("https://cn.bing.com/dict/search?q=" + this.searchKey);
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url(../css/YelHead.css);
</style>
