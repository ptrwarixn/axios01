<template>
  <div id="app">
    <img alt="" src="" />
    
    <HelloWorld msg="What's your favorite artist " />

  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";


export default {
  name: "App",
  components: {
    HelloWorld,

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
  margin-top: 60px;
}
.bg{
    background-image: url(https://wall.alphacoders.com/big.php?i=1032786);
    background-size: cover;
  }
</style>
