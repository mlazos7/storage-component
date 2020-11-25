<template>
  <div id="app">
    <div id="wrapper">
      <StorageRemaining />
    </div>
    <Attribution />
  </div>
</template>

<script>
import StorageRemaining from "./views/StorageRemaining";
import Attribution from "./components/Attribution";

export default {
  name: "App",
  components: {
    StorageRemaining,
    Attribution,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
body {
  margin: 0;
  padding: 0;
  background: no-repeat url("./assets/bg-desktop.png") 0% 115%;
  background-size: 100%;
  background-color: #0c122c;
}
#app {
  width: 100vw;
  height: 100vh;
  text-align: center;
  margin: 0 auto;
  font-size: 14px;
  font-family: "Raleway", sans-serif;
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

p {
  color: #dbd9ff;
}
</style>
