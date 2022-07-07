<template >
  <template v-for="(name, index) in names" :key="index">
    <div > {{name}} </div>
    <hr>
  </template>
  
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
     names: ['nom1', 'nom2', 'nom3'] 
    }
    
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


</style>
