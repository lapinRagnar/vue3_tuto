<template>
  <h1>reactivity and toRef - exemple 2</h1>
  <h2>{{state.firstName}} {{state.lastName}}</h2>
  <h2>ou la 2e methode - pas de reactivite quand on modifie la variable</h2>
  <h2>{{firstName}} {{lastName}}</h2>
  <h2>il faut utiliser toRefs pour avoir la reactivité</h2>
</template>

<script>

import {reactive} from 'vue'
export default {
  name: 'DemoTwo',
  setup(){
    const state = reactive({
      firstName: 'bruce',
      lastName: 'wayne'
    })

    setTimeout(() => {
      state.firstName = 'clark'
      state.lastName = 'david'
      console.log(state);
    }, 2000);

    return{
        state,
        firstName: state.firstName,
        lastName: state.lastName,
    }
  }

}
</script>

<style>

</style>