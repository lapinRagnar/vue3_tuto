<template>
  <h2>provide inject</h2> <hr>
  <h3>parent component - nom = {{name}}</h3>
  <h3>parent component - count = {{count}}</h3>
  <h3>parent component - hero = {{firstName}} et {{lastName}}</h3>
  
  <button @click="incrementCount">incrementer</button>
  <br>

  <child-a></child-a>
</template>

<script>

import {provide, ref, reactive, toRefs} from 'vue'
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

    const count = ref(0)
    const state = reactive({
        firstName: 'bruce',
        lastName: 'lee'
    })

    provide('c_count', count)
    provide('c_hero', state)

    provide('incrementCount', incrementCount)

    function incrementCount(){
      count.value++
    }

    return {
      count,
      ...toRefs(state),
      incrementCount
    }

  }
}
</script>

<style>

</style>