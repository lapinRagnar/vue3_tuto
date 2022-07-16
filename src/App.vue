<template >
  <h1>Composition api</h1>
  <ComputedCompo/>
</template>


<script>

import ComputedCompo from './components/ComputedCompo.vue'


export default {
  name: 'App',
  components: {ComputedCompo},
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
