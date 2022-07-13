<template >

  <NameList>
    <template v-slot:defalut="slotProps">
      {{slotProps.firstName}} - {{slotProps.lastName}}
    </template>
  </NameList>

</template>

<script>

import NameList from './components/NameList.vue'

export default {
  name: 'App',
  components: { NameList },
  data(){
    return {

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
