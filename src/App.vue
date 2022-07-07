<template >

  <p>fonction ajouter - {{add(2, 2, 2)}} </p>
  <p>fonction multiplication - {{ multiply(2) }} </p>  

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      baseMultiplication: 5
    }    
  },
  methods: {
    add(a, b, c) {
      return a + b + c
    },
    multiply(num) {
      return num * this.baseMultiplication
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
