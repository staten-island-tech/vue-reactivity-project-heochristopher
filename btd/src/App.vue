<template>
<div class="container">
 <h2>{{color}}</h2>
    <Grid :gridColor= this.myColor />
    <Color @btnClick="getColor"/>
    <Tools/>
</div>
   
</template>

<script>

import Color from './components/Color'
import Grid from './components/Grid'
import Tools from './components/Tools'


export default {
  name: 'App',
  components: {
    Grid,
    Color,
    Tools
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
}

</style>
