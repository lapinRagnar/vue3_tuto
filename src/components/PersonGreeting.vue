<template>
  <h2>person greeting</h2>
  <div>bonjour {{fullName}}</div>
  <button @click="sendEvent">call heroes</button>
</template>

<script>

import {computed} from 'vue'

export default {
  name: 'PersonGreeting',
  props: ['firstName', 'lastName'],
  setup(props, context){

    const fullName = computed(()=>{    
    return `${props.firstName} ${props.lastName}`
    })

    function sendEvent(){
      context.emit('callHeroes', fullName)
    }

    return {
      fullName,
      sendEvent
    }
  },

}
</script>

<style>

</style>