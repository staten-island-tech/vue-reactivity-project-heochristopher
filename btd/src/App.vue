<template>
<div class="container">
 <Grid/>
    <Colors/>
</div>
   
</template>

<script>

import Grid from './components/Grid'
import Colors from './components/Colors'

export default {
  name: 'App',
  components: {
    Grid,
    Colors
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
