<template>
  <h2>props avec - option api</h2>
  <div>
    <input type="text" placeholder="first name" v-model="firstName" >
    <input type="text" placeholder="last name" v-model="lastName">
  </div>

  <PersonGreeting :firstName="firstName" :lastName="lastName" />

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

    return {
        firstName,
        lastName,
    }
  }
}
</script>

<style>

</style>