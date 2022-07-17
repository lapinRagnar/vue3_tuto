<template >
  <h1>Composition api</h1>
  <ProvideInject/>
</template>


<script>

import ProvideInject from './components/ProvideInject.vue'


export default {
  name: 'App',
  components: {ProvideInject},
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
