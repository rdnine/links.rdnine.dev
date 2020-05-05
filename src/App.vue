<template>
  <div id="app">
    <div class="root">
      <Title v-bind:key="info.title" v-bind:img="info.title.img" v-bind:username="info.title.username" v-bind:name="info.title.name" v-bind:job="info.title.job"/>
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
body {margin: 0; background-color: #FEFFFF; box-sizing: border-box; font-family: 'Roboto', sans-serif;}

a {font-family: 'Roboto', sans-serif; font-weight: 700; font-size: 20px; line-height: 20px;}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #feffff;
  background-color: #06d6a0;
  position: relative;
  width: 100%;
  max-width: 560px;
  min-height: 100vh;
  margin: auto;
  padding: 60px 30px;
  box-shadow: 0 0 15px rgba(0,0,0,0.3);
  box-sizing: border-box;
}

.root {
  display: block;
  position: relative;
  margin-bottom: 60px;
}

.tree {
  width: 100%;
  max-width: 450px;
  margin: auto;
}

@media screen and (max-width: 500px) {
  .tree {
    max-width: 320px;
  }
}
</style>
