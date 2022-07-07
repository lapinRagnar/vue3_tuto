<template>
  <div v-for="(a, index) in actors" :key="index"> 
    <h1>{{ a.name}}</h1>
    <p v-for="(m,i) in a.movies" :key="i"> {{ m }} </p>
  </div>
  
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      actors: [
        {
          name: 'jean claude vandame',
          movies: ['kick boxing', 'karate man']
        },
        {
          name: 'dicaprio',
          movies: ['titanic', 'je ne sais pas']
        }
      ]
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
