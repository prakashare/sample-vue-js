<template>
  <div id="app">
    <img width="64px" height="64px" src="./assets/logo.png" /> <Page01 />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Page01 from "./components/Page01";

export default {
  name: "App",
  components: {
    Page01
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 10px;
}
</style>
