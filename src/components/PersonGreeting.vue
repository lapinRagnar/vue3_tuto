<template>
  <h2>person greeting</h2>
  <div>bonjour {{fullName}}</div>
</template>

<script>


export default {
  name: 'PersonGreeting',
  props: ['firstName', 'lastName'],
  computed:{
    fullName(){
        return `${this.firstName} ${this.lastName}`
    }
  }
}
</script>

<style>

</style>