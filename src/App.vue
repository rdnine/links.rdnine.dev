<template>
  <div id="app"></div>
</template>

<script>
import Title from "./components/Title";
import Leaf from "./components/Leaf";
import info from "../public/data.json";

export default {
  name: "App",
  data() {
    return info;
  },
  components: {
    Title,
    Leaf
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
