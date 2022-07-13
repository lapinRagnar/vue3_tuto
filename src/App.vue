<template >
  <div>Bonjour</div>
  <card-compo content="card content 1"/>
  <card-compo content="card content 2" />
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
