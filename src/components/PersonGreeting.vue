<template>
  <h2>person greeting</h2>
  <div>bonjour {{firstName}} {{lastName}}</div>
</template>

<script>


export default {
  name: 'PersonGreeting',
  props: ['firstName', 'lastName']
}
</script>

<style>

</style>