<template>
  <h1>avec option api</h1>
  <h3>mon nom est {{name}}</h3>
  <button @click="setName">changer le nom</button>
  <hr>
  <h1> fonction avec setup - composition api</h1>
  <h2>{{count}}</h2>
  <button @click="incrementCount">incrementer</button>
</template>

<script>

import {ref} from 'vue'
export default {
  name: 'MethodsCompo',
  data() {
    return {
        name: 'lapin'
    }
  },
  methods: {
    setName(){
        this.name = 'ragnar'
    }
  },
  setup(){
    const count = ref(0)
    
    function incrementCount(){
        count.value++
    }

    return {
        count,
        incrementCount
    }
  }

}
</script>

<style>

</style>