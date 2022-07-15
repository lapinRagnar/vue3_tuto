<template>
  <div>data compo</div>
  <h2>options api - {{o_firstName}}</h2>
  <h2>composition api- {{c_firstName}}</h2>
</template>

<script>

import ref from 'vue'

export default {
  name: 'DataCompo',
  setup(){
    const c_firstName = ref('clark')
    c_firstName.value = 'diana'
    const greet = `bonjour ${c_firstName.value}`
    console.log(c_firstName);

    return {
      c_firstName, // ou c_firstName seulemet (shorthand)
      greet  
    } 
  },
  data(){
    return { 
      o_firstName: 'bruce'    
    }
  }
}
</script>

<style>

</style>