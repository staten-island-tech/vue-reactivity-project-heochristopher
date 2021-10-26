<template>
  <div class="grid">
    <div
      v-for="color in colors"
      :key="color"
      class="grid-box"
      :id="`${color}`"
      :style="`background-color: ${color}`"
      @click='changeColor(`${color}`)'
    >
    </div>
  </div>
</template>

<script>
export default {
  name: "Color",
  data() {
    return {
      colors: [
        "blue",
        "red",
        "yellow",
        "green",
        "black",
        "purple",
        "orange",
        "pink",
      ],
    }
  },
   methods: {
        changeColor(color) {
          this.$emit(color)
            console.log(color)
        }
    },
};
</script>

<style scoped>
.grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-column-gap: 5px;
    width: 30%;
}

.grid-box {
    padding: 0px;
    margin: 0px;
    height: 40px;
    width: 40px;
   border: 1px solid #000;
   
}
</style>