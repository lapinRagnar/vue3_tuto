<template >
  <h1>Composition api</h1>
  <TemplateRef/>

</template>


<script>

import TemplateRef from './components/TemplateReference.vue'


export default {
  name: 'App',
  components: {TemplateRef},
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
