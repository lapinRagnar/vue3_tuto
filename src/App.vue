<template >
  <div>Bonjour</div>
  <InputCompo />
</template>

<script>

import InputCompo from './components/Input.vue'

export default {
  name: 'App',
  components: { InputCompo },
  data(){
    return {
      name: ''
    }    
  },
  methods: {},
  computed: {},
  watch: {}
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}


</style>
