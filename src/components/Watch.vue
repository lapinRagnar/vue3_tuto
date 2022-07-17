<template>
  <h1>option api </h1>
  <div>
    <input type="text" placeholder="name" v-model="name">
  </div>

  <h1>watch avec composition api - ref</h1>
  <input type="text" placeholder="First Name" v-model="firstName">



</template>

<script>

import {ref, watch} from 'vue'

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

    watch(firstName, (newValue, oldValue)=>{
      console.log('oldValue', oldValue)
      console.log('newValue', newValue);
    })

    return {
        firstName
    }
  }

}
</script>

<style>

</style>