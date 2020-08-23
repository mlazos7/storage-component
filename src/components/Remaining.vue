<template>
  <div class="container">
    <div class="progress">
      <div class="progress-title">
        <p>
          You’ve used
          <b>{{usedSpace}} GB</b> of your storage
        </p>
        <p><b>{{freeSpace}} GB Left</b></p>
      </div>
      <img src="./../assets/progress.png" alt="remaining" />
      <div class="progress-limits">
        <p>
          <b>0 GB</b>
        </p>
        <p>
          <b>{{capacity}} GB</b>
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    capacity: String,
    usedSpace: String,
  },

  computed: {
    freeSpace: function () {
      return this.capacity - this.usedSpace;
    },
  },
};
</script>

<style scoped>
.container {
  margin-left: 30px;
  width: 540px;
  min-height: 154px;
  background-color: #1e2d69;
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  box-sizing: border-box;
  border-radius: 10px;
  align-self: flex-end;
}

.container p {
  line-height: 16px;
}

.progress {
  margin: 0 auto;
}

.progress-title{
    display:flex;
    justify-content: space-between;
}
.progress-limits {
  display: flex;
  justify-content: space-between;
}

.progress-limits p {
  margin-top: 5px;
}
</style>