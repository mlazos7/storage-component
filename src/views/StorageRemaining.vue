<template>
  <div class="wrapper-storage">
    <TheTitle />
    <Remaining capacity="1000" usedSpace="875" />
  </div>
</template>

<script>
import TheTitle from "./../components/TheTitle";
import Remaining from "./../components/Remaining";

export default {
  name: "StorageRemaining",
  components: {
    TheTitle,
    Remaining,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.wrapper-storage {
  margin: 0 auto;
  display: flex;
}
</style>
