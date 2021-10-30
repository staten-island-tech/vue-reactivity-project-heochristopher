<template>
<div class="container">
  <h1>{{userColor}}</h1>
  <div class="grid">
    
    <div
      v-for="color in colors"
      :key="color"
      class="grid-box"
      :id="`${color}`"
      :style="`background-color: ${color}`"
      @click="$emit('btnClick', color), displayColor(color)"
    >
    </div>
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
      userColor: 'black'
    }
  },
   methods: {
     displayColor(color) {
       this.userColor = color
     }
   }
};
</script>

<style scoped>
.conatiner{
  display: flex;
  overflow-y:hidden;
}

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