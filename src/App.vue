<template >

  <h1>{{name}}</h1>
  <div>
    <button v-on:click="name = 'batman'">Changer le nom</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      name: 'lapin ragnar'
    }    
  },
  methods: {

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
