<template>
  <h2 v-bind:class="isPromoted && 'promoted'">on ajoute une classe css promoted quand isPromoted=true</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      isPromoted: true
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
.promoted{
  color: #95bc4c;
  font-size: 40px;
}

</style>
