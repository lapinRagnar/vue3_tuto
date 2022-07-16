<template>
  <h1>option api- v-model</h1>
  <input type="text" placeholder="first name" v-model="fName">
  <input type="text" placeholder="last name" v-model="lName">
  <p>{{fName}} {{lName}}</p>

  <hr>

  <h1>composition api- v-model</h1>
  <input type="text" placeholder="hero name" v-model="heroName">
  <input type="text" placeholder="first name" v-model="firstName">
  <input type="text" placeholder="first name" v-model="lastName">
  
  <p style="color: orage">{{heroName}} - {{firstName}} + {{lastName}}</p>

</template>

<script>

import {ref, reactive, toRefs} from 'vue'

export default {
  name: 'VModel',
  data(){
    return {
      fName: '',
      lName: ''
    }
  },
  setup(){
    const heroName = ref('')
    const state = reactive({
        firstName: '',
        lastName: '',
    })

    return {
        heroName,
        ...toRefs(state)
    }
  }
}
</script>

<style>

</style>