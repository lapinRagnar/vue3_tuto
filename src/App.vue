<template >

  <h1>Nom : {{ nom }}</h1>
  <div>
    <button @click="changerNom">Changer le nom</button>
  </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      nom: 'lapin'
    }    
  },
  methods: {
    changerNom(event){
      this.nom = 'sauve souris'
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
