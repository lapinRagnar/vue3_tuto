<template>
  <div v-if="num === 0">number is 0</div>
  <div v-else>number is not 0</div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      num: 5
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
