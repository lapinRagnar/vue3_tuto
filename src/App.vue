<template>
  <template v-if="afficher">
    <div>Afficher</div>
    <div>plusieurs ligne</div>
    <div>avec une seule condition</div>
  </template>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      afficher: true
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
