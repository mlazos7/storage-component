<template>
  <div class="hello">
    <!-- <h1>{{ msg }}</h1> -->
    <p>
You’ve used {{usedSpace}} GB of your storage
    </p>
    <p>
    {{freeSpace}} GB Left
    </p>
    <p>
    0 GB - {{capacity}} GB
    </p>
    
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    capacity: String,
    usedSpace: String,
  },

  computed: {
    freeSpace: function () {
      return this.capacity - this.usedSpace
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello{
  margin: 0 auto;
}
</style>
