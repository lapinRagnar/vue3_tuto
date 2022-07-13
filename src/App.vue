<template >
  <CardCompo>
    <template v-slot:header>
      <h1>Header qui vient du parent</h1>
    </template>

    <template v-slot:default>
      <div>Bonjour du parent</div>
    </template>

    <template v-slot:footer>
      <div>le pied de page du parent</div>
      <div><button>valider</button></div>
    </template>


  </CardCompo>
  



</template>

<script>

import CardCompo from './components/Card.vue'
export default {
  name: 'App',
  components: { CardCompo },
  data(){
    return {
      name: ''
    }    
  },
  methods: {},
  computed: {},
  watch: {}
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}


</style>
