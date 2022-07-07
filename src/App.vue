<template>
  <h2 v-bind:style="{color: couleur, backgroundColor: fond }">ajout inline style - avec un objet</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      couleur: 'red',
      fond: 'yellow'
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
.sold_out{
  color: #95bc4c;
  font-size: 40px;
  height: 100px;
}

.new{
  color: rebeccapurple;
  background-color: #95bc4c;
}

</style>
