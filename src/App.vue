<template>
  <div v-for="(name, index) in names" :key="name"> {{index}} - {{ name}}</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      names: ['bruce lee', 'clark kent', 'batman']
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
