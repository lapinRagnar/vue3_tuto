<template >
  <h1>Composition api</h1>
  <WatchCompo/>
</template>


<script>

import WatchCompo from './components/Watch.vue'


export default {
  name: 'App',
  components: {WatchCompo},
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
