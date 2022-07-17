<template >
  <h1>Composition api</h1>
  <PersonCompo/>

</template>


<script>

import PersonCompo from './components/Person.vue'


export default {
  name: 'App',
  components: {PersonCompo},
  data(){
    return {}    
  },
  methods: {},
  computed: {},
  watch: {}
}
</script>

<style scoped>

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
  }

</style>
