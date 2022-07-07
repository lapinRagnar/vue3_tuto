<template>
  <h2 v-bind:class="isNew ? 'new' : 'sold_out'">on ajoute une classe css avec condition ternaire</h2>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      isNew: true
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
}

.new{
  color: rebeccapurple;
  background-color: #95bc4c;
}

</style>
