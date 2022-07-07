<template >

  <h1>compteur # {{count}}</h1>
  <div>
    <button v-on:click="incrementer(1)">incrementer 1</button>
    <button v-on:click="incrementer(5)">incrementer 5</button>
    <button v-on:click="decrementer(1)">decrementer 1</button>
    <button v-on:click="decrementer(10)">decrementer 10</button>
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
    incrementer(num){
      return this.count += num
    },
    decrementer(num){
      return this.count -= num
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
