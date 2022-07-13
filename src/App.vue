<template >

  <h4>bonjour parent</h4>
  <child-styles></child-styles>
</template>

<script>

import ChildStyles from './components/ChildStyles.vue'

export default {
  name: 'App',
  components: { ChildStyles },
  data(){
    return {

    }    
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
  h4{
    color: orange;
  }


</style>
