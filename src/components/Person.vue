<template>
  <h2>reusability - composition api</h2>


  <PersonGreeting :firstName="firstName" :lastName="lastName" @callHeroes="callHeroes"/>

</template>

<script>

import PersonGreeting from './PersonGreeting.vue'
import {ref} from 'vue'

export default {
  name: 'PersonCompo',
  components: { PersonGreeting },
  setup(){
    const firstName = ref('')
    const lastName = ref('') 

    function callHeroes(hero){
      alert(`calling ==> ${hero}`)
      console.log(hero);
    }

    return {
      firstName,
      lastName,
      callHeroes
    }
  },
  emits: ['callHeroes']
}
</script>

<style>

</style>