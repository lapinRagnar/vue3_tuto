<template >
  <div>Composition api</div>
  <data-compo/>
</template>


<script>

import DataCompo from './components/DataCompo.vue'


export default {
  name: 'App',
  components: { DataCompo},
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
