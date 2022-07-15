<template>
  <h1>reactivity and toRef - exemple 1</h1>
  <h2>{{name}}</h2>
</template>

<script>

import {ref} from 'vue'

export default {
  name: 'DemoOne',
  setup(){
    const name = ref('lapin')
    setTimeout(() => {
      name.value = 'ragnar'
    }, 2000);

    return {
        name
    }
  }
}
</script>

<style>

</style>