<template>
  <div id="app">
    <div id="wrapper">
      <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
      <StorageRemaining usedSpace="901" capacity="1000" />
      <Attribution/>
    </div>
  </div>
</template>

<script>
import StorageRemaining from "./components/StorageRemaining";
import Attribution from "./components/Attribution";

export default {
  name: "App",
  components: {
    StorageRemaining,
    Attribution
  },
};
</script>

<style>
body {
  margin: 0;
  padding: 0;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background-color: #0c122c;
  width: 100vw;
  height: 100vh;
  text-align: center;
  margin: 0 auto;
}
#wrapper {
  width: 100%;
  height: 100%;
  display: flex;
  margin: 0 auto;
  box-sizing: border-box;
  flex-direction: column;
  justify-content: center;
}

p{
    color: #DBD9FF
}
</style>
