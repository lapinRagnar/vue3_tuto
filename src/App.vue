<template>
  <div v-for="(info, key, index) in myInfo" :key="index"> {{index}} - {{key}} - {{info}} </div>
  
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
     myInfo: {
      name: 'lapin',
      language: 'vue'
     }
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
