<template>
  <h1>avec option api</h1>
  <h3>mon nom est {{name}}</h3>
  <button @click="setName">changer le nom</button>

  <hr>
  
  <h1> fonction avec setup - composition api</h1>
  <h2>{{count}}</h2>
  <button @click="incrementCount">incrementer</button>

  <hr>

  <h1>exemple avec - reactive et toRefs</h1>
  <h2>{{first}} + {{last}}</h2>
  <button @click="changeHero">change hero</button>

</template>

<script>

import {ref, reactive, toRefs} from 'vue'
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
    const state = reactive({
        first: 'bruce',
        last: 'wayne'
    })
    
    function incrementCount(){
        count.value++
    }

    function changeHero(){
        state.first = 'lapin'
        state.last = 'ragnar'
    }

    return {
        count,
        incrementCount,
        ...toRefs(state),
        changeHero
    }
  }

}
</script>

<style>

</style>