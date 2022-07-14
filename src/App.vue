<template >
  <parent-compo></parent-compo>
</template>

<script>

import ParentCompo from './ParentCompo.vue'


export default {
  name: 'App',
  components: {ParentCompo },
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
