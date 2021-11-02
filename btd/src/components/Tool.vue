<template>
  <div class="container">
      <div class="tool" id="pen" @click="$emit('changeTool', 'pen')"></div>
      <div class="tool" id="eraser" @click="$emit('changeTool', 'eraser')"></div>
  </div>
</template>

<script>
export default {
  name: "Tool",
  data() {
    return {
    }
  },
   methods: {
   }
}
</script>

<style scoped>
#pen {
  background-image: url('../assets/pen.png');
  width: 40px;
  height: 40px;
  background-size: cover;
}
#eraser {
  background-image: url('../assets/eraser.png');
   width: 40px;
  height: 40px;
  background-size: cover;
}
</style>