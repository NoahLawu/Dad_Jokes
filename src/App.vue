<template>
  <DadJokes></DadJokes>
</template>

<script>
import DadJokes from "./components/DadJokes.vue";

export default {
  name: "App",
  components: {
    DadJokes,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  background-color: #ffb6c1;
}

html,
body {
  height: 100%;
  margin: 0;
  padding: 0;
  overflow-x: hidden;
}
</style>
