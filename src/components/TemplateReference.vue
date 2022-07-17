<template>
  <h2>templateRef avec - composition api</h2>
  <input type="text" placeholder="tapez texte" ref="inputRef">
  
  
</template>

<script>

import {ref, onMounted} from 'vue'

export default {
  
  name: 'TemplateRefere',

  setup(){
    const inputRef = ref(null)
    
    onMounted(()=>{
      inputRef.value.focus()
    })

    return {
        inputRef,
    }
  }
}
</script>

<style>

</style>