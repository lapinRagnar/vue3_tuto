<template >
  <h1>Composition api</h1>
  <demo-one></demo-one>
  <demo-two/>
</template>


<script>

import DemoOne from './components/DemoOne.vue'
import DemoTwo from './components/DemoTwo.vue'


export default {
  name: 'App',
  components: {DemoOne, DemoTwo},
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
