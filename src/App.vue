<template>
  <div v-for="(f, index) in fullName" :key="index"> {{index}} - {{ f.first}} {{ f.last }}</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      fullName: [
        {first: 'piso', last: 'beloha'},
        {first: 'lava', last: 'rambo'},
        {first: 'be', last: 'menimenina'},
      ]
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
