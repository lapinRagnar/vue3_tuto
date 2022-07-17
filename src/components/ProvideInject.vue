<template>
  <h2>provide inject</h2> <hr>
  <h3>parent component - nom = {{name}}</h3>
  <child-a></child-a>
</template>

<script>

import {provide} from 'vue'
import ChildA from './ChildA.vue'

export default {
  name: 'ProvideInject',
  components: { ChildA },
  data(){
    return {
      name: 'lapin'    
    }
  },
  provide(){
    return {
        userName: this.name
    }
  },
  setup(){
    provide('c_userName', 'lapinbe')
  }
}
</script>

<style>

</style>