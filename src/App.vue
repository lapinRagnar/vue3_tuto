<template >

  <h1>compteur # {{count}}</h1>
  <div>
    <button @click="ajouter(4, $event)">ajouter</button>
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
    ajouter(num, event){
      this.count += num
      console.log('evenement object', event);
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
