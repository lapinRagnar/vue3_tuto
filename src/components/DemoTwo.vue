<template>
  <h2>il faut utiliser toRefs pour avoir la reactivité</h2>
  <h2>{{firstName}} {{lastName}}</h2>
</template>

<script>

import {reactive, toRefs} from 'vue'
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

    return toRefs(state)
  }

}
</script>

<style>

</style>