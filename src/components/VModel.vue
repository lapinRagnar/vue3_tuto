<template>
  <h1>option api- v-model</h1>
  <input type="text" placeholder="first name" v-model="fName">
  <input type="text" placeholder="last name" v-model="lName">
  <p>{{fName}} {{lName}}</p>
</template>

<script>
export default {
  name: 'VModel',
  data(){
    return {
      fName: '',
      lName: ''
    }
  }
}
</script>

<style>

</style>