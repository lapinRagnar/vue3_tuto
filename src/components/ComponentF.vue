<template>
  <div>Component F</div>
  <div>Component F username - {{ username }}</div>
</template>

<script>
export default {
  name: 'ComponentF',
  inject: ['username']
}
</script>

<style>

</style>