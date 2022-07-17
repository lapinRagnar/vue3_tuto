<template>
  <h1>option api </h1>
  <div>
    <input type="text" placeholder="name" v-model="name">
  </div>

  <h1>immediate watch avec composition api - ref - une source</h1>
  <input type="text" placeholder="First Name" v-model="firstName">

  <h1>watch avec composition api - ref - plusieurs sources</h1>
  <input type="text" placeholder="First Name" v-model="firstName">
  <input type="text" placeholder="Last Name" v-model="lastName">


  <h1>watch avec composition api - reactive et toRefs - modifie tte les propriete </h1>
  <input type="text" placeholder="reactive first Name" v-model="fName">
  <input type="text" placeholder="reactive last Name" v-model="lName">

</template>

<script>

import {ref, toRefs, watch, reactive} from 'vue'

export default {
  name: 'WatchCompo',
  data(){
    return{
        name: ''
    }
  },
  watch:{
    name(newValue, oldValue){
        console.log('oldValue', oldValue);
        console.log('newValue', newValue);
    }
  },
  setup(){
    const firstName = ref('')
    const lastName = ref('wayne')

    const state = reactive({
      fName: '',
      lName: ''
    })

    // modifie toute les proprieté
    // watch(()=>{return {...state}}, function(newValue, oldValue){
    //   console.log('fName oldValue', oldValue.fName)
    //   console.log('fName newValue', newValue.fName)
    //   console.log('fName oldValue', oldValue.fName)
    //   console.log('fName oldValue', newValue.fName)
    // })

    watch(()=>state.fName, function(newValue, oldValue){
        console.log('newValue', newValue)
        console.log('oldValue', oldValue);
    })


    watch([firstName, lastName], (newValues, oldValues)=>{
      console.log('firstname oldValue', oldValues[0])
      console.log('firstname newValue', newValues[0])
      console.log('lastName oldValue', oldValues[1])
      console.log('lastname newValue', newValues[1])
    }, {immediate: true})

    return {
        firstName,
        lastName,
        ...toRefs(state)
    }
  }

}
</script>

<style>

</style>