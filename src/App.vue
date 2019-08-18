<template>
  <div id="app">
    <h1>{{msg}}</h1>
    <Gameview />
  </div>
</template>

<script>
import Gameview from "./components/Gameview.vue";
export default {
  name: "app",
  data() {
    return { msg: "Welcome to TicTacToe Game" };
  },
  components: { Gameview }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
