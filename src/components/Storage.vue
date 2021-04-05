<template>
  <div class="storage-container">
    <div class="progress">
      <div class="progress-title">
        <p>
          You’ve used
          <b>{{ usedSpace }} GB</b> of your storage
        </p>
        <div class="popup">
          <div class="col-1">
            {{ freeSpace }}
          </div>
          <div class="col-2">GB LEFT</div>
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
          <b>{{ capacity }} GB</b>
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