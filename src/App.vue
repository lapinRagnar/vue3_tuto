<template >
  <h1>Composition api</h1>
  <LifecycleOptions/>
  <LifecycleComposition/>
</template>


<script>

import LifecycleOptions from './components/LifecycleOptions.vue'
import LifecycleComposition from './components/LifecycleComposition.vue'


export default {
  name: 'App',
  components: {LifecycleOptions, LifecycleComposition},
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
