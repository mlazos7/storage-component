<template>
  <div class="container">
    <div class="progress">
      <div class="progress-title">
        <p>
          You’ve used
          <b>{{usedSpace}} GB</b> of your storage
        </p>
        <div class="popup">
          <!-- <img src="./../assets/popup.svg" alt="remaining"> -->
          <div class="col-1">
            <p>
              <b>{{freeSpace}}</b>
            </p>
          </div>
          <div class="col-2">
            <b><p>GB Left</p></b>
          </div>
        </div>
      </div>
      <div class="progress-image">
        <img src="./../assets/progress.png" alt="progress" />
      </div>
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
  line-height: 16px;
}

.progress {
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.progress-title {
  display: flex;
  justify-content: space-between;
  position: relative;
  margin-bottom: 15px;
}

.progress-title p {
  margin: 0;
  padding: 0;
}

.popup {
  background-image: url("./../assets/popup.svg");
  width: 179px;
  height: 93px;
  display: flex;
  justify-content: space-evenly;
  position: absolute;
  right: 0;
  bottom: 0;
}

.popup p {
  color: black;
  padding-top: 25px;
}

.col-1 {
  font-size: 40px;
}

.col-2 {
  color: #0c122c;
  font-size: 12px;
  letter-spacing: 1px;
  opacity: 50%;
}

.progress-limits {
  display: flex;
  justify-content: space-between;
}

.progress-limits p {
  margin-top: 5px;
  margin-bottom: 0px;
}
</style>