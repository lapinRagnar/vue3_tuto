<template >
  <h1>Composition api</h1>
  <methods-compo></methods-compo>
</template>


<script>

import MethodsCompo from './components/MethodsCompo.vue'


export default {
  name: 'App',
  components: {MethodsCompo},
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
