<template>
<div class="container">
  <h1>{{displayColor}}</h1>
  <Grid :gridColor= this.myColor />
  <Color @btnClick="getColor"/>
  <Tool @changeTool="chooseTool"/>
</div>
   
</template>

<script>

import Color from './components/Color'
import Grid from './components/Grid'
import Tool from './components/Tool'

export default {
  name: 'App',
  components: {
    Grid,
    Color,
    Tool
  },
  data(){
    return{
      myColor: '',
      displayColor: 'black'
    }
  },
  methods: {
    getColor(color) {
      this.myColor = color
      this.displayColor = color
    },
    chooseTool(tool) {
      if(tool === 'pen' && this.myColor != '#fff') {
        return
      } else if (tool === 'pen' && this.myColor === '#fff') {
        this.myColor = '#000'
        this.displayColor = 'black'
      } else {
        this.myColor = '#fff'
        this.displayColor = 'eraser'
      }
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
  overflow-y:hidden;
}

.container {
  display: flex;
  justify-content: space-between;
  align-content: flex-start;
  flex-wrap: wrap;
}

</style>
