<template >

  <h1>compteur # {{count}}</h1>
  <div>
    <button v-on:click="incrementer">incrementer</button>
    <button v-on:click="decrementer">decrementer</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      count: 0
    }    
  },
  methods: {
    incrementer(){
      return this.count += 1
    },
    decrementer(){
      return this.count -= 1
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
