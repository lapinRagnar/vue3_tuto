<template >

  <h1>nom: {{nom}}</h1>
  <h1>compteur # {{count}}</h1>

  <div>
    <button @click="modifierNom(), ajouter(4, $event)">ajouter</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      count: 0,
      nom: 'rabitro'
    }    
  },
  methods: {
    ajouter(num, event){
      this.count += num
      console.log('evenement object', event)
    },
    modifierNom(){
      this.nom = 'ra la la la la!'
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
