<template>
  <h1>option api</h1>
  <input type="text" placeholder="first name" v-model="fName">
  <input type="text" placeholder="last name" v-model="lName">
  <p>options api fullName - {{fName}} et {{lName}} => {{fullName}}</p>
  <h1>computed</h1>


</template>

<script>

export default {
  name: 'ComputedCompo',
  data(){
    return{
      fName: '',
      lName: ''
    }
  },
  computed:{
    fullName(){
      return `${this.fName} -${this.lName}`
    }
  }

}
</script>

<style>

</style>