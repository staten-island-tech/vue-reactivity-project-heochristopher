<template>
<div class="container">
  <Grid :gridColor= this.myColor />
  <Color @btnClick="getColor"/>
</div>
   
</template>

<script>

import Color from './components/Color'
import Grid from './components/Grid'

export default {
  name: 'App',
  components: {
    Grid,
    Color,
  },
  data(){
    return{
      myColor: ''
    }
  },
  methods: {
    getColor(color) {
      this.myColor = color
      console.log(this.myColor)
    }
  }
}
</script>

<style>
html {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}

.container {
  display: flex;
  justify-content: space-between;
  align-content: flex-start;
  flex-wrap: wrap;
}

</style>
