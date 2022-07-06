<template>
  <div v-bind:id="nomId"></div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      nomId: "mon_super_id_a_ajouter_dans_le_tag"
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
