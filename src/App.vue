<template>
  <div id="app">
    <div id="wrapper">
      <div class="wrapper-storage">
        <TheTitle />
        <Storage capacity="1000" usedSpace="875" />
      </div>
    </div>
    <Attribution />
  </div>
</template>

<script>
import Attribution from "./components/Attribution";
import TheTitle from "./components/TheTitle";
import Storage from "./components/Storage";
import "./styles.scss";
export default {
  name: "App",
  components: {
    Attribution,
    TheTitle,
    Storage,
  },
};
</script>
