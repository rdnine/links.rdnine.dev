<template>
  <div id="app">
    <div class="root">
      <div class="title">
        <Title v-bind:key="info.title" v-bind:img="info.title.img" v-bind:username="info.title.username" v-bind:name="info.title.name" v-bind:job="info.title.job"/>
      </div>
    </div>
    <div class="tree">
      <Leaf
        v-for="link in info.links"
        v-bind:key="link"
        v-bind:link="link.href"
        v-bind:label_under="link.label_under"
        v-bind:label_top="link.label_top"
      ></Leaf>
    </div>
    <div class="logo">
      <img v-bind:key="info.app" :src="info.app.logo" :alt="info.app.name">
    </div>
  </div>
</template>

<script>
import Title from "./components/Title";
import Leaf from "./components/Leaf";
import info from "../public/data.json";

export default {
  name: "App",
  data() {
    return {info};
  },
  components: {
    Title,
    Leaf
  }
};
</script>

<style>
* {box-sizing: border-box;}

body {margin: 0; background-color: #17242A; font-family: 'Roboto', sans-serif;}

a {font-family: 'Roboto', sans-serif; font-weight: 700; font-size: 20px; line-height: 20px;}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #17242A;
  background-color: #feffff;
  position: relative;
  display: block;
  width: 100%;
  max-width: 560px;
  min-height: 100vh;
  margin: auto;
  box-shadow: 0 0 15px rgba(0,0,0,0.3);
}

.root {
  display: block;
  position: relative;
}

.title {
  width: 100%;
  padding: 45px 30px;
}

.tree {
  width: 100%;
  max-width: 450px;
  margin: auto;
  padding: 30px 15px 120px;
}

.logo {
  padding: 30px 15px;
  display: block;
  position: absolute;
  left: 0;
  right: 0;
  bottom: 0;
  margin: auto;
}

.logo img {
  max-width: 75px;
}

@media screen and (max-width: 500px) {
  .tree {
    max-width: 320px;
  }
}
</style>
