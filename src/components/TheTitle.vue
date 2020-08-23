<template>
  <div class="container">
      <img src="./../assets/logo.svg" alt="logo">
      <div class="links">
          <img src="./../assets/icon_1.svg" alt="icon_1">
          <img src="./../assets/icon_2.svg" alt="icon_2">
          <img src="./../assets/icon_3.svg" alt="icon_3">
      </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
.container{
    width: 350px;
    height: 200px;
    background-color: #1E2D69;
    display:flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: flex-start;
    padding-left: 40px;
    box-sizing: border-box;
    border-radius: 10px;
}

.links img{
    padding-right: 18px;
}
</style>