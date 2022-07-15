<template>
  <div>data compo</div>
  <h2>options api - {{o_firstName}} {{o_lastName}} ## {{o_heroName}}</h2>
  <h2>composition api - {{c_firstName}}</h2>
  <h2>composition api - {{c_firstName}} {{c_lastName}} ** {{c_heroName}}</h2>
  <h2>composition - {{greetHero}}</h2>
  <h2>composition - reactive - {{state.firstName}} {{state.lastName}} ## {{state.heroName}} </h2>
  <h2>composition - reactive - {{reactiveGreetHero}}</h2>
</template>

<script>

import {ref, reactive} from 'vue'

export default {
  name: 'DataCompo',
  data(){
    return { 
      o_firstName: 'bruce',
      o_lastName: 'wayne',
      o_heroName: 'batman'    
    }
  },
  setup(){
    const c_firstName = ref('clark')
    const c_lastName = ref('kent')
    const c_heroName = ref('superman')

    const state = reactive({
      firstName: 'princess',
      lastName: 'diana',
      heroName: 'wonder woman',
    })

    const reactiveGreetHero = `bonjour, ${state.firstName} ${state.lastName} ++ ${state.heroName}`

    const greet = `bonjour ${c_firstName.value}`
    console.log(c_firstName)

    const greetHero = `bojour, ${c_lastName.value} ${c_firstName.value} ## ${c_heroName.value}  `

    return {
      c_firstName, // ou c_firstName seulemet (shorthand)
      greet,
      c_lastName,
      c_heroName,
      greetHero,
      reactiveGreetHero,
      state  
    } 
  },


}
</script>

<style>

</style>