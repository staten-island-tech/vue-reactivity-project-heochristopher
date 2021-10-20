<template>
<div class='container'>
  <img :src='img' alt="">
  <div class="sidebar-container">
    <h2>Change Map</h2>
    <div class="monkeys-container">
      <h2>Monkeys</h2>
    </div>
  </div>
  <button v-on:click='changeMap'>Change Map</button>
</div>
</template>

<script>
export default {
    name: 'Game',
    data() {
        return {
            img: require("../assets/maps/monkey-meadow.png")
        }
    },
    methods: {
        changeMap() {
            this.img = require('../assets/maps/chutes.png')
        }
    }
}
</script>

<style scoped>
.container {
  display: flex;
}
img {
  width: 80%;
}
</style>