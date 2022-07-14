<template >
  <div>template ref</div>
  <TemplateRef></TemplateRef>
</template>


<script>


import TemplateRef from './components/TemplateRef.vue'

export default {
  name: 'App',
  components: { TemplateRef },
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
