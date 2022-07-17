<template>
  <h1>option api</h1>
  <input type="text" placeholder="first name" v-model="fName">
  <input type="text" placeholder="last name" v-model="lName">
  <p>options api fullName - {{fName}} et {{lName}} => {{fullName}}</p>
  
  <h1>composition api - computed</h1>
  
  <input type="text" placeholder="first name" v-model="refFirstName">
  <input type="text" placeholder="last name" v-model="refLastName">
  <p>composition api - computed fullName => {{refFullName   }}</p>


  <h1>composition api - reactive, toReffs, computed</h1>
  
  <input type="text" placeholder="first name" v-model="reactiveFirstName">
  <input type="text" placeholder="last name" v-model="reactiveLastName">
  <p>composition api - reactive fullName => {{reactiveFullName}}</p>

</template>

<script>

import {ref, computed, reactive, toRefs} from 'vue'

export default {
  name: 'ComputedCompo',
  data(){
    return{
      fName: '',
      lName: ''
    }
  },
  computed:{
    fullName(){
      return `${this.fName} -${this.lName}`
    }
  },
  setup(){
    const refFirstName = ref('')
    const refLastName = ref('')

    const refFullName = computed(function(){
      return `${refFirstName.value} ${refLastName.value}`
    })

    const state = reactive({
      reactiveFirstName: '',
      reactiveLastName: '',
    })

    const reactiveFullName = computed(function(){
      return `${state.reactiveFirstName} ${state.reactiveLastName} `
    })

    return {
        refFirstName,
        refLastName,
        refFullName,
        ...toRefs(state),
        reactiveFullName
    }
  }

}
</script>

<style>

</style>