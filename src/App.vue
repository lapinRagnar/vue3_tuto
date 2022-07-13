<template >
  <div>Bonjour</div>
  <CardCompo></CardCompo>
  <card-compo>Card content 2</card-compo>
  <card-compo>
    <h2>Card content 2</h2>
  </card-compo>
  <card-compo>Card content 3</card-compo>
  
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
