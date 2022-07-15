<template >
  <div>click counter</div>
  <ClickCounter></ClickCounter>
  <HoverCounter/>
</template>


<script>


import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'

export default {
  name: 'App',
  components: { ClickCounter, HoverCounter },
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
